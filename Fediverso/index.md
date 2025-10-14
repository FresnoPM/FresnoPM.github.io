
# HOLA, MUNDO FED

## Tu primer cuenta

Sacar una cuenta en el fediverso es como pelar una naranja (podés tener todas las que quieras).

- Si ya tenés una cuenta y querés federarla con otras andá derecho a <a href="#FEDERACIÓN">FEDERACIÓN</a>
- Si ya tenés claro cómo funciona todo y querés los 3 pasos simples andá a <a href="##TLDR">TL;DR</a>

Elegir con cuidado porque no los podés cambiar:

- mi-user sería como tu nombre, el que te dio tu mamá
- mi-instancia vendría a ser el apellido 

> Si por algún motivo necesitás hacerlo se puede crear una nueva cuenta y exportando/importando tus datos... se puede hacer pero tratemos de no meternos ahí

Podés cambiar tantas veces como quieras:

- mi-nick sería como te llaman tus amigos
- mi-banner es la imagen que va en el encabezado de tu perfil
- mi-avatar: la carita que aparece al lado de mi-nick en cada publicación
- mi-bio: texto introductorio, descripción sobre vos o lo que tus visitantes podrán encontrar en tus publicaciones

## Criterios
Estos datos están publicados en la página instancia/about de cada server

- reglas del servidor: algunas más estrictas que otras, es importante que estés de acuerdo porque si lo las seguís te van a echar
- ubicación geográfica de los servers: esto influye en la eficiencia y el tiempo que toma publicar
- si tienen un tópico específico: por ejemplo puede ser un server dedicado a publicar fotos de gatos, todas las publicaciones que no sean fotos de gatos deberán ser privadas
- cantidad de usuarios registrados
- idioma
- features activadas: no todos los servers tienen las mismas funcionalidades o configuraciones, esto lo deciden sus owners o admins, por ejemplo algunos tienen un límite máximo de caracteres por publicación, otros no permiten polls...y así
- donde estén tus amiwis
- Otras ¿cuáles?

## Directorios de instancias

Existen varios, y muchas instancias existentes no están listadas pero acá hay suficientes para chusmear

Listas de servers o instancias:

- https://joinmastodon.org/servers
- https://instances.social
- https://pixelfed.org/servers
- https://gram.social/web/directory
- https://pleroma.social/#featured-instances
- https://fedidb.com/
- https://fedidb.org
- https://fedi.directory/
- https://mastodon.help/instances/en
- https://the-federation.info/

Diferentes softwares que usan Activity pub:

Mi recomendación: No te compliques demasiado con esto, ya va a haber tiempo para ir afinando la puntería.

- https://en.wikipedia.org/wiki/Fediverse#Software
- https://the-federation.info/protocol/4 <-- anda muuuuuuuuuy lento

 
 ___


# FEDERACIÓN

No hace falta tener una cuenta en cada instancia para interactuar con usuarios radicados en otras. Si tus amis están en otra instancia de la fed podés poner @su-user@su-instancia en el buscador, va a aparecer su cuenta en el listado y desde ahí podés empezar a seguirla.
Va a lucir así

> https://[mi-instancia]/@[su-user]@[su-instancia]


> Por ejemplo puedo seguir a una cuenta radicada en pixelfed.social desde gram.jp o desde mastodon.social y seguir una cuenta radicada en mastodon.la desde pixelfed.social. En este caso desde el universo pixel sólo se pueden visualizar contenido multimedia publicado desde otras cuentas, pero es un detalle. **Lo importante es que se puede sin usar puentes externos.**

Si quiero vincularme con cuentas que están fuera de la FED (sus instancias corren en servers que no tienen protocolo ActivityPub) puedo usar puentes. Los puentes son una cosa de locos, hay muchos, acá te cuento cómo usar bridgy que me pareció el más completo. Si te da mucha curiosidad el tema acá podés leer sobre puenteo entre servidores: https://en.wikipedia.org/wiki/Network_bridge.

## Federación usando FED.BRID.GY 

Hice esta guía para quienes quieren federar entre BlueSky y Mastodon porque es mi caso. Eventualmente, si llega a surgir la necesidad lo haré para otras plataformas, pero creo que con esto es suficiente.

Para que vean mis publicaciones de mi cuenta original (desde OTRA-APP) debo crear una cuenta puenteada a partir de mi cuenta original.

Para eso debo seguir al BRIDGY local desde mi cuenta. Esto hará que BRIDGY me empiece a seguir.

- Desde MSTD  https://mi-instancia/@bsky.brid.gy@bsky.brid.gy
- Desde BSKY https://bsky.app/profile/ap.brid.gy


BRIDGY creará a partir de mi cuenta original una nueva cuenta puenteada que es:

> @[mi-user-original].[mi-instancia-original]@bsky.brid.gy

Los usuarios de otras apps podrán visualizarla desde una url que es 

> https://OTRA-APP/@[mi-user-original].[mi-instancia-original]@bsky.brid.gy

Esta cuenta puenteada será una copia de la original. Tendrá mismo avatar, mismo banner, misma bio con una línea extra agregada en la bio que hace fácil de reconocerla como puenteada.
En este perfil se verán todas las publicaciones realizadas en mi cuenta original a partir del momento en que se empezó el vínculo con la cuenta de BRIDGY correspondiente.

Todos los usuarios de la OTRA-APP podrán ver mi cuenta, interactuar con ella, ver las publicaciones e interactuar con ellas tanto como su OTRA-APP lo permita. 

Desde mi cuenta original sólo podré ver (e interactuar con) cuentas de OTRA-APP y sus publicaciones si éstas están, a su vez, vinculadas con la cuenta de BRIDGY correspondiente a su app. Tampoco voy a poder ver las interacciones de users de OTRA-APP en los posts de mi cuenta puenteada ni recibir notificaciones a menos que estén vinculados con BRIDGY para permitir que yo los vea desde mi cuenta original.

Si quiero que un user de OTRA-APP se conecte con el fediverso y no lo hace por su cuenta le puedo mandar un mensaje privado a mi BRIDGY local que diga sólamente @otro-usuario@su-nstancia y BRIDGY le solicitará por mensaje privado que se una. Máximo de solicitudes diarias: 10. https://fed.brid.gy/docs#dm-request

## TLDR

Pasos:

1) Seguir a tu BRIDGY local. Esto crea tu cuenta puenteada. Te va a llegar el link por mensaje privado desde la cuenta de dicho BRIDGY local.
2) Compartí esta cuenta puenteada con tus amiwis de la otra plataforma.
3) Pediles a estas personas que también sigan a su BRIDGY local de la plataforma donde estén.

ÉXITO! Ya están conectades!



___


# EXTRAS 



## Activar/Desactivar

Desde  https://fed.brid.gy/settings puedo cambiar el status mi cuenta ya puentada (activa/inactiva). Tarda ~5 minutos en realizarse los cambios. Después de cambiar el status debo esperar 5 minutos antes de volver a cambiarlo.

Desde esa página se puede también cambiar el Bluesky handle en caso de que tengas un dominio propio (opcional) y activar/desactivar DM notifications from unbridged accounts. O sea, si quiero recibir o no mensajes privados notificándome de si alguna cuenta no puenteada (no vinculada con su BRIDGY local) interactuó con mi cuenta puenteada o alguna de sus publicaciones. Más detalles sobre cómo funciona todo esto acá https://fed.brid.gy/docs

Si quiero desactivar por completo mi puenteo debo dejar de seguir y eliminar seguidor o bloquear seguidor a la cuenta local de BRIDGY. El puenteo de publicaciones funciona únicamente si BRIDGY local te sigue.

## Links piolas para gente techie

https://indieweb.org/bridge_all_the_things

¿Cómo armar un form html para seguir a un usuario miembro del fediverso?
https://indieweb.org/Bridgy_Fed#How_to_add_a_follow_form

___


# YO

Armé este documento porque, a raíz de declaraciones políticas de la CEO de la plataforma, no quiero seguir en bsky. El tema es que en BSKY encontré una hermosa comunidad y no quiero renunciar a ella sólo porque sus posturas no sean tan firmes como las mías. Mi simpatía por el software libre, la federación y demás utopías tecnológicas siempre me atrajeron pero sus limitaciones económicas y prácticas me hicieron dejarlas de lado. Pasó muy poco desde la última vez que sentí la imperiosa necesidad de abandonar una plataforma donde había desarrollado fuertes vínculos y una identidad personal y laboral robusta por su cambio de dirección (cuando el nuevo dueño de equis hizo un gesto imperdonable). Mis espacios de comunidad online son muy importantes para mi y no quiero volver a tener que elegir. 

Tampoco me siento cómoda hoy con el server que elegí, aún siento que no soy dueña de _"Mis cosas"_ ahí porque al minuto que tenga un conflicto con alguna de las autoridades voy a tener que irme. Aún no es un problema pero no tengo ganas de llegar a ese punto. En este momento no estoy en condiciones de crear mi propio server, como muches de uds me han sugerido. Es un trabajo enorme y no estoy del todo segura de que esa sea la mejor manera de lograr la sensación de autonomía y seguridad que necesito para estar tranquila.
Eventualmente, cuando haya estabilizado todo este asunto y haya testeado cuán viable es federar entre mstd y bsky voy a dejar bsky por completo. Pero hoy no es el día.

Si querés consultarme dudas que surgieron a raíz de este artículo, querés debatir puntos de vista (relevantes para el artículo) o creés que tenés algo copado para agregar podés contactarte conmigo. 

Por ahora me encontrás en 

- https://mastodon.uy/@Siboney
- https://bsky.app/profile/candycandem.bsky.social

Con cariño, _De-Lulu_