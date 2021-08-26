---
title: Pruebas de validación para almacenes en línea de tipo 2 de incorporación
description: En este tema se describen las pruebas que Microsoft realizará para validar la tienda en línea de Tipo 2. Microsoft requiere que ejecute estas pruebas antes de enviar un candidato para lanzamiento. La tienda en línea debe superar correctamente estas pruebas para publicarse.
ms.assetid: 1da51772-9711-4913-b05d-830fabe49da2
keywords:
- Reproductor de Windows Media Tiendas en línea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab2cb1b4d44b1bd3c6289311c6b276de7c75ed1bcd955431796a36d272811942
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901384"
---
# <a name="validation-tests-for-on-boarding-type-2-online-stores"></a>Pruebas de validación para almacenes en línea de tipo 2 de incorporación

En este tema se describen las pruebas que Microsoft realizará para validar la tienda en línea de Tipo 2. Microsoft requiere que ejecute estas pruebas antes de enviar un candidato para lanzamiento. La tienda en línea debe superar correctamente estas pruebas para publicarse.

> [!Note]  
> Si el almacén es de tipo 1 en lugar de tipo 2, puede usar este tema como guía para comprender el ámbito de las pruebas de certificación que se tratan para los almacenes de tipo 1. Para obtener el conjunto completo de pruebas para almacenes de tipo 1, póngase en [contacto Soporte técnico de Microsoft](https://support.microsoft.com/ph/7763#tab0).

 

En este tema se incluyen las siguientes secciones.

-   [Lista de comprobación de pruebas](#test-checklist)
    -   [Preparación del pase de prueba](#test-pass-preparation)
-   [Entorno de prueba](#test-environment)
-   [Instalación y configuración](#configuration-and-setup)
    -   [Configuración de una máquina de pruebas](#setting-up-a-test-machine)
    -   [Configuración de una tienda](#setting-up-a-store)
    -   [Creación de una cuenta](#creating-an-account)
    -   [Configuración del almacenamiento en caché de credenciales](#setting-up-credential-caching)
-   [Adquisición de contenido](#content-acquisition)
    -   [Contenido de streaming](#streaming-content)
    -   [Obtener contenido](#obtaining-content)
    -   [Contenido de grabación](#burning-content)
    -   [Transferencia de contenido](#transferring-content)
-   [Características de la tienda](#store-features)
    -   [Administración de una cuenta](#managing-an-account)
    -   [Administración del Centro de información](#managing-the-info-center)
-   [Interacción del almacén](#store-interaction)
    -   [Yielding to the Active Store](#yielding-to-the-active-store)
    -   [Impedir que el almacén probado tome el control del almacén activo](#preventing-the-tested-store-from-taking-over-the-active-store)
    -   [Acceso a un almacén en High-Contrast automático](#accessing-a-store-in-high-contrast-mode)
    -   [Protección de un almacén](#securing-a-store)

## <a name="test-checklist"></a>Lista de comprobación de pruebas

Use la lista de comprobación de la tabla siguiente para validar la tienda en línea de Tipo 2 que desea que se introduzca.



Prueba

Windows XP

Windows Vista

Windows 7

Resultado (pass/fail/not applicable)

32

64

32

64

32

64

1. Compruebe que el software se instala.

2. Compruebe que el software se desinstala.

3. Compruebe que el software no se ejecuta en la bandeja.

4. Compruebe que la pestaña de almacén funciona.

5. Compruebe que el almacén tiene una opción para crear una nueva cuenta.

6. Compruebe que la cuenta creada puede iniciar sesión.

7. Compruebe que el almacén tiene una opción para guardar la información del usuario.

8. Compruebe que el almacenamiento en caché de credenciales está presente y funcionando.

9. Compruebe que se le pidan credenciales al usuario si no están almacenadas en caché.

10. Compruebe que todos los tipos disponibles de flujo de contenido.

11. Compruebe que el contenido se reproduce en Microsoft Reproductor de Windows Media.

12. Compruebe que un precio calculado es correcto.

13. Compruebe que el contenido comprado se descarga en la biblioteca.

14. Compruebe que los metadatos se descargan para la compra.

15. Compruebe que los derechos de uso de los medios son correctos para la compra.

16. Compruebe que el contenido comprado puede reproducirse.

17. Compruebe que al hacer clic en el **botón** **Comprar** o Comprar, cambia a la tienda.

18. Compruebe que se ha descargado el contenido comprado.

19. Compruebe que el contenido comprado se puede comprar.

20. Compruebe que el recuento de la grabación se ha decrementado.

21. Compruebe que el contenido se puede transferir a otro equipo.

22. Compruebe que el contenido se transfiere a un dispositivo.

23. Compruebe que el recuento de sincronización se ha decrementado.

24. Compruebe que el historial de compras realiza un seguimiento de las compras anteriores.

25. Compruebe que se puede restaurar una compra anterior.

26. Compruebe la funcionalidad de un almacén para administrar varios equipos.

27. Compruebe que el Centro de información está desactivado de forma predeterminada.

28. Compruebe que el Centro de información tiene información multimedia en el área que se está reproduciendo.

29. Compruebe que los vínculos se desplazan al almacén.

30. Compruebe que el almacén probado se produce en el almacén activo.

31. Compruebe que el almacén probado no toma el control del almacén actual.

32. Compruebe que el almacén es accesible en modo de contraste alto.

33. Compruebe que el almacén es seguro.



 

### <a name="test-pass-preparation"></a>Preparación del pase de prueba

Antes de ejecutar una prueba, debe asegurarse de que el almacén y las cuentas de prueba están listos para las pruebas. Debe determinar la siguiente información antes de que se inicie el paso. Si puede determinar la información con unos días de antelación a la prueba, el paso se ejecutará de forma más eficaz.

-   Determine la siguiente información sobre las cuentas de prueba proporcionadas por el almacén:
    -   Las cuentas y contraseñas funcionan para permitir que un usuario inicie sesión
    -   Las cuentas se financian correcta y adecuadamente para cada tipo de modo de negocio que ofrece la tienda.
    -   Las cuentas son válidas para que se puedan probar todas las configuraciones regionales o existen cuentas para cada configuración regional si las cuentas no pueden realizarse entre configuraciones regionales.
-   Determine qué configuraciones regionales se probarán.
-   Determine qué idiomas se probarán.
-   Determine la siguiente información sobre el entorno de prueba:

    -   Almacenes en directo que funcionan con Windows XP, Windows Vista y Windows 7
    -   El almacén no vivo que se probará
    -   Compruebe que el almacén no en directo que se va a probar está visible en todas las versiones del sistema operativo y en todas las versiones de Reproductor de Windows Media plataforma.

-   Determine la siguiente información sobre el almacén que se probará:

    -   Nombre de almacén
    -   Gráficos y etiqueta esperados del logotipo de la pestaña de la tienda
    -   ¿La tienda está disponible para todas las versiones del sistema operativo?
    -   ¿Se trata de una nueva versión de la tienda en pruebas?
    -   ¿Está la tienda en pruebas un almacén de tipo 1 o tipo 2?
    -   ¿Ha cambiado el tipo de almacén?

-   Determine en qué versiones y plataformas del sistema operativo tiene previsto probar la tienda.
-   Determine que el instalador y el complemento funcionan en todas las versiones y plataformas del sistema operativo que se probarán.
-   Determine si se requiere un documento de navegación.
-   Determine la siguiente información sobre los medios que ofrece la tienda:

    -   Formatos
    -   ¿Se requiere algún software propietario?
    -   ¿Debe probar todos los tipos de medios o solo un subconjunto de tipos de medios?

-   Determine la siguiente información sobre los derechos de uso multimedia:

    -   ¿Los medios de almacenamiento tienen protección de contenido?
    -   Si es así, determine el tipo de protección de contenido que tienen los medios.
    -   Si es así, determine el comportamiento protegido esperado.
    -   ¿Los derechos de uso multimedia incluyen el uso compartido de equipo a equipo?
    -   Derechos de sincronización
    -   Derechos de grabación
    -   Los derechos de reproducción
    -   Fechas de expiración, si las hay

-   Determine si tiene suficientes medios (un catálogo lo suficientemente grande) para proporcionar un ejemplo significativo.
-   Determine cuál es el paso de fase: RC 0, cumplimiento, y así sucesivamente.
-   Determine si la prueba supera un tipo determinado: regresión, humo, y así sucesivamente.

## <a name="test-environment"></a>Entorno de prueba

Debe realizar pruebas en las siguientes configuraciones:

-   Microsoft Reproductor de Windows Media 11 en Windows XP con sistemas operativos Service Pack 3 (SP3) de 32 y 64 bits
-   Reproductor de Windows Media 11 en Windows operativos Vista de 32 y 64 bits (32 bits Reproductor de Windows Media)
-   Microsoft Reproductor de Windows Media 12 en Windows operativos de 7 32 y 64 bits (32 bits Reproductor de Windows Media)

Aunque debe realizar pruebas en todas las versiones y plataformas del sistema operativo enumeradas, las versiones de 32 bits de Windows Vista y Windows 7 son las versiones de sistema operativo de destino prioritario. Debe probar la instalación de cualquier software en todas las plataformas.

Las capturas de pantalla de este tema usan un almacén ficticio, Proseware, para demostrar el uso de la interfaz de usuario.

## <a name="configuration-and-setup"></a>Instalación y configuración

En las secciones siguientes se describe cómo configurar y configurar las pruebas de validación para la entrada de una tienda en línea de tipo 2.

### <a name="setting-up-a-test-machine"></a>Configuración de una máquina de pruebas

Realice los pasos siguientes para configurar una máquina de prueba:

1.  Apunte el equipo de prueba a los servidores de prueba de contenido agregando una clave del Registro específica del almacén.
2.  Establezca los valores del **cuadro de diálogo Opciones regionales** y de idioma en la configuración regional y de idioma adecuadas. Para establecer el idioma, seleccione la **pestaña Formatos** y, a continuación, seleccione el idioma en el **cuadro combinado** Formato actual. Para establecer la región, seleccione la **pestaña Ubicación** y, a continuación, seleccione la región en el **cuadro combinado Ubicación** actual. Además, en el caso de los almacenes que requieren la instalación de un complemento o software personalizado específico del almacén, es posible que tenga que cambiar la configuración regional del sistema al idioma de la configuración regional de la tienda para facilitar la instalación. El instalador de software debe admitir caracteres de byte único y doble y debe ejecutarse en cualquier configuración regional. Debe probar en la configuración regional nativa. Para establecer la configuración regional nativa, abra el  cuadro de diálogo **Región** e idioma, seleccione la pestaña Administrativo y, a continuación, haga clic en el botón Cambiar configuración **regional** del sistema como se muestra en la siguiente captura de pantalla. Al hacer clic en este botón se **muestra el cuadro de diálogo Región Configuración** idioma. El **cuadro combinado Configuración regional del sistema** actual de ese cuadro de diálogo cambia la configuración regional del sistema.

    En las capturas de pantalla siguientes se muestran las pestañas en las que puede establecer la región y el idioma:

    ![captura de pantalla del cuadro de diálogo de opciones regional e idioma](images/reg-lang-opt.png)

    ![captura de pantalla que muestra cómo cambiar la configuración regional del sistema actual](images/reg-lang-settings.png)

3.  Desactive la vista del Centro de información de una tienda estableciendo Reproductor de Windows Media para reproducir una visualización. La principal diferencia entre las plataformas es que, en Reproductor de Windows Media 11, empieza haciendo clic en Ahora reproduciendo **,** mientras que en Reproductor de Windows Media 12, empieza haciendo clic con el botón derecho en la ventana principal.

    La siguiente captura de pantalla muestra la secuencia de opciones de menú que reproduce una visualización Reproductor de Windows Media 11:

    ![captura de pantalla que muestra cómo reproducir una visualización en el Reproductor de Windows Media 11](images/wmp11-visual.png)

    La siguiente captura de pantalla muestra la secuencia de opciones de menú que reproduce una visualización en Reproductor de Windows Media 12:

    ![captura de pantalla que muestra cómo reproducir una visualización en el Reproductor de Windows Media 12](images/wmp12-visual.png)

### <a name="setting-up-a-store"></a>Configuración de una tienda

En primer lugar, realice los pasos siguientes para configurar un almacén y, a continuación, realice los pasos que siguen los pasos iniciales para comprobar la configuración del almacén:

1.  Inicie Reproductor de Windows Media y espere varios segundos para adquirir el archivo de AllServices.xml más reciente.
2.  Para Windows XP y Windows Vista, para seleccionar una tienda en línea, primero haga clic en la pestaña que se divide entre la vista Guía multimedia y la vista Tiendas en línea. A continuación, en el menú, haga clic en Examinar todas **las** tiendas en línea y seleccione la tienda haciendo clic en su icono en la lista de tiendas. Para Windows 7, haga clic en el botón del panel de navegación de la biblioteca que se divide entre el botón **Guía** multimedia y el botón **Tiendas en** línea. A continuación, en el menú, haga clic en Examinar todas **las** tiendas en línea y seleccione la tienda haciendo clic en su icono en la lista de tiendas.

    En la siguiente captura de pantalla se muestra cómo seleccionar una tienda en línea Reproductor de Windows Media 11:

    ![captura de pantalla que muestra cómo seleccionar una tienda en línea en el Reproductor de Windows Media 11](images/wmp11-set-store.png)

    En la siguiente captura de pantalla se muestra cómo seleccionar una tienda en línea Reproductor de Windows Media 12:

    ![captura de pantalla que muestra cómo seleccionar una tienda en línea en el Reproductor de Windows Media 12](images/wmp12-set-store.png)

3.  Siga las instrucciones de la tienda para instalar cualquier software adicional necesario para usar la tienda.

**Para comprobar la configuración del almacén**

1.  Compruebe que el software se instala.

    Compruebe que el complemento OCX o cualquier otro software de la tienda se descarga e instala sin errores.

2.  Compruebe que el software se desinstala.

    Compruebe que, en Panel de control,  en el elemento Programas y características, el  software que instala la tienda aparece en la lista Desinstalar o cambiar un programa y compruebe que puede desinstalarlo de esta lista sin errores.

3.  Compruebe que el software no se ejecuta en la bandeja del sistema.

    Compruebe que ningún software de la tienda agrega iconos al área de notificación del programa (en la barra de tareas a la izquierda del reloj) antes del consentimiento del cliente para descargar el software de la tienda.

    La experiencia básica de almacenamiento no debe requerir la instalación de software adicional. Debe estar disponible una experiencia multimedia básica, como los medios de streaming. Algunas tiendas instalan software adicional, como los administradores de descarga, para obtener una experiencia multimedia premier. estos almacenes pueden tener iconos en la bandeja del sistema si los iconos representan aplicaciones independientes de Reproductor de Windows Media.

4.  Compruebe que la pestaña de almacén funciona.

    Compruebe que la pestaña tienda cambia para indicar el almacén seleccionado.

    Para Windows XP y Windows Vista con Reproductor de Windows Media 11, compruebe que el nombre y el icono de la tienda están visibles en el fondo oscuro Reproductor de Windows Media 11.

    Para Windows 7 con Reproductor de Windows Media 12, compruebe que el nombre del almacén y el icono están visibles en el panel de navegación de la biblioteca, en el menú contextual del selector de servicios.

    Compruebe que el almacén aparece en la parte superior de la lista de selectores de tienda del menú.

    > [!Note]  
    > No habrá ninguna opción **de menú** Agregar servicio actual al menú si el almacén de tipo 2 es el almacén destacado (predeterminado) de la región.

     

    La siguiente captura de pantalla muestra el menú que aparece al hacer clic en la pestaña de la esquina superior derecha Reproductor de Windows Media 11:

    ![captura de pantalla que muestra la pestaña de la tienda en el Reproductor de Windows Media 11](images/wmp11-verify-store.png)

    En la siguiente captura de pantalla se muestra el menú que aparece al hacer clic en el botón dividir situado en la esquina inferior izquierda Reproductor de Windows Media 12:

    ![captura de pantalla que muestra la pestaña de la tienda en el Reproductor de Windows Media 12](images/wmp12-verify-store.png)

### <a name="creating-an-account"></a>Creación de una cuenta

**Para comprobar la configuración de la cuenta**

1.  Compruebe que el almacén tiene una opción para crear una nueva cuenta y, a continuación, siga las instrucciones del almacén para crear una nueva cuenta.

    En la captura de pantalla siguiente se resalta **un botón Crear** nueva cuenta como podría aparecer en Reproductor de Windows Media 11:

    ![captura de pantalla que muestra cómo comprobar la configuración de la cuenta para el Reproductor de Windows Media 11](images/wmp11-verify-account.png)

    En la siguiente captura de pantalla se resalta **un botón** Crear nueva cuenta como podría aparecer en Reproductor de Windows Media 12:

    ![captura de pantalla que muestra cómo comprobar la configuración de la cuenta para el Reproductor de Windows Media 12](images/wmp12-verify-account.png)

2.  Compruebe que puede iniciar sesión en la cuenta que ha creado.

### <a name="setting-up-credential-caching"></a>Configuración del almacenamiento en caché de credenciales

En primer lugar, realice los pasos siguientes para configurar el almacenamiento en caché de credenciales y, a continuación, realice los pasos que siguen los pasos iniciales para comprobar la configuración del almacenamiento en caché de credenciales:

1.  En la página de inicio de sesión, escriba las credenciales y seleccione la opción para guardar la información del usuario.
2.  Compruebe que la página de inicio de sesión tiene una casilla que permite al usuario almacenar en caché las credenciales.
3.  El almacenamiento en caché de credenciales opcional es un punto de seguridad importante. El almacenamiento en caché automático de credenciales puede exponer información de identificación personal de los usuarios que inician sesión en un equipo compartido o público. Debe proteger la información del cliente al ofrecer una casilla que representa el almacenamiento en caché opcional.

**Para comprobar el almacenamiento en caché de credenciales**

1.  Compruebe que la tienda tiene una casilla para la **opción Guardar mi información de** usuario.

    1.  Cierre Reproductor de Windows Media.
    2.  Vuelva Reproductor de Windows Media e intente descargar contenido.

2.  Compruebe que el almacenamiento en caché de credenciales está presente y funcionando.

    1.  Cerrar sesión en la tienda.
    2.  Cierre Reproductor de Windows Media.
    3.  Vuelva Reproductor de Windows Media e intente descargar contenido.

3.  Compruebe que se le pidan credenciales al usuario si no están almacenadas en caché.

    Después de firmar y, a continuación, intentar usar la tienda, se debe solicitar al cliente las credenciales.

## <a name="content-acquisition"></a>Adquisición de contenido

En esta sección se describen las distintas formas de adquirir contenido y cómo comprobar que ese contenido se adquirió.

### <a name="streaming-content"></a>Contenido de streaming

Transmita todos los tipos de contenido disponibles desde la tienda. Por ejemplo, transmitir contenido de radio, vídeo, audio y vistas previas.

**Para comprobar el contenido de streaming**

1.  Compruebe que todos los tipos disponibles de flujo de contenido.

2.  Compruebe que el contenido se reproduce en Reproductor de Windows Media y no en ningún otro reproductor o control.

### <a name="obtaining-content"></a>Obtener contenido

En primer lugar, realice los pasos siguientes para comprar contenido y, a continuación, realice los pasos que siguen los pasos iniciales para comprobar la compra y comprobar que el contenido se ha descargado:

1.  Inicie Reproductor de Windows Media.
2.  Inicie sesión en la cuenta de prueba.
3.  Vaya al contenido que se va a comprar.
4.  Siga el procedimiento específico de la tienda para comprar contenido.

**Para comprobar el contenido comprado y descargado**

1.  Compruebe que el precio calculado es correcto.

    Compruebe que el precio es correcto, especialmente al comprar varios fragmentos de contenido a la vez, y compruebe que la información de saldo de la cuenta se actualiza correctamente después de la compra. Algunos contenidos se pueden comprar como pistas únicas y otros solo como álbumes. Compruebe que el precio del álbum no sea mayor que la suma de las pistas individuales.

2.  Compruebe que el contenido adquirido se descarga en la biblioteca.

    Cuando se complete la descarga, vaya al contenido descargado en la biblioteca Reproductor de Windows Media datos. El contenido descargado se encuentra en la biblioteca del usuario actual.

    -   Para Windows XP y Windows Vista con Reproductor de Windows Media 11, el contenido descargado aparece en el  panel de navegación de la biblioteca, en el pivote Biblioteca y, a continuación, en **Canciones**.
    -   Para Windows 7 con Reproductor de Windows Media 12, el contenido que se descarga en la biblioteca de Reproductor de Windows Media aparece en el panel de navegación Reproductor de Windows Media en **Música**.

3.  Compruebe que los metadatos se descargan para la compra.

    Asegúrese de que las columnas siguientes aparecen en la biblioteca Reproductor de Windows Media (agrégrelas si no es así):

    -   Album Artist
    -   Título
    -   Título del álbum
    -   Proveedor de contenido
    -   Género

    Se deben rellenar las columnas anteriores. El contenido debe tener un arte de álbum. Sin embargo, no es necesario que el arte del álbum pase las pruebas de validación.

4.  Compruebe que los derechos de uso de los medios son correctos para la compra.

    Para cada pista descargada, haga clic con el botón derecho en la pista, seleccione **Propiedades** y, a continuación, seleccione la **pestaña Derechos de uso multimedia.**

    La tienda puede optar por proteger su contenido con derechos de uso multimedia o puede optar por no proteger el contenido. La **pestaña Derechos de uso** multimedia refleja ese estado enumerando las restricciones o indicando que el contenido no está protegido. El almacén debe comunicar su plan más actual para los derechos de uso multimedia. Debe comprobar los resultados reales con este comportamiento esperado.

    Las licencias de derechos multimedia deben entregarse previamente. No es necesario que el cliente reprodgue el contenido ni que pase por algún otro proceso para obtener la licencia. Debe comparar los derechos de uso multimedia específicos con lo que la tienda ha comunicado al cliente según corresponda. Los derechos deben ser transferibles a al menos otros dos equipos. Los clientes deben poder grabar y sincronizar sus medios.

    En la siguiente captura de pantalla se muestran los derechos de uso multimedia de un archivo protegido:

    ![captura de pantalla que muestra los derechos de uso multimedia de un archivo protegido](images/media-rights-protected.png)

    Si el contenido no está protegido, la **pestaña Derechos de uso** multimedia indica este hecho.

    En la captura de pantalla siguiente se muestran los derechos de uso multimedia de un archivo no protegido:

    ![captura de pantalla que muestra los derechos de uso multimedia de un archivo no protegido](images/media-rights-not-protected.png)

5.  Compruebe que se reproduce el contenido adquirido.

    Compruebe que el contenido descargado se reproduce en Reproductor de Windows Media.

    Reproducir cualquier contenido que se haya comprado en la tienda y que resida en la biblioteca local, o transmitir una vista previa.

    Realice los pasos siguientes para comprar contenido en Windows XP y Windows Vista con Reproductor de Windows Media 11:

    1.  Haga clic en **la pestaña Reproducción** ahora.
    2.  En el panel de lista, coloque el puntero del mouse para mantener el puntero sobre la imagen del álbum con el fin de mostrar el **vínculo Comprar.**
    3.  Haga clic **en Comprar**.

    La siguiente captura de pantalla muestra la ubicación del **vínculo Comprar** en Reproductor de Windows Media 11:

    ![captura de pantalla que muestra cómo comprar contenido en el Reproductor de Windows Media 11](images/wmp11-verify-buy-play.png)

    Realice los pasos siguientes para comprar contenido en Windows 7 con Reproductor de Windows Media 12:

    1.  En el modo de biblioteca, haga clic en **la pestaña** Reproducir.
    2.  En la lista de reproducción, en el cuadro de música del álbum, haga clic **en Comprar.**

    En la siguiente captura de pantalla se muestra cómo comprar contenido en Reproductor de Windows Media 12:

    ![captura de pantalla que muestra cómo comprar contenido en el Reproductor de Windows Media 12](images/wmp12-verify-buy-play.png)

6.  Compruebe que al hacer clic **en Comprar** **o Comprar,** cambia a la tienda.

    El Reproductor de Windows Media debe cambiar a la tienda en la vista de biblioteca y cargar la experiencia de compra de la tienda.

    A continuación, debe seguir comprando la pista.

7.  Compruebe que, después de hacer **clic en Comprar** o **Comprar,** el contenido se descarga.

    Compruebe que los derechos de uso multimedia son adecuados para el contenido adquirido y sus metadatos, y compruebe que se reproduce la pista. En general, este método de compra debe tener los mismos resultados que otros métodos.

### <a name="burning-content"></a>Contenido de grabación

En primer lugar, realice los pasos siguientes para grabar el contenido adquirido (copiar el contenido adquirido en un CD o DVD que se pueda escribir) y, a continuación, realice los pasos que siguen los pasos iniciales para comprobar que el contenido se encuentra en estado grave:

> [!Note]  
> Antes de grabar una pista comprada, anote su número de quemas para poder comprobar más adelante si el recuento disminuye después de grabar la pista.

 

1.  Haga clic en **la pestaña Grabar.**
2.  Arrastre las pistas adquiridas a **la lista de grabación.**
3.  Haga clic en **el botón Iniciar grabación.**

En la siguiente captura de pantalla se muestra **la** Lista de grabación en el lado derecho de la pantalla y el botón Iniciar grabación debajo de **la** lista de grabación Reproductor de Windows Media 11: 

![captura de pantalla que muestra cómo grabar contenido en el Reproductor de Windows Media 11](images/wmp11-verify-burn.png)

En la siguiente captura de pantalla se muestra cómo aparece la lista de grabación en Reproductor de Windows Media  12 después de  arrastrar una pista a la lista de grabación y se muestra el botón Iniciar grabación en la parte superior de la pestaña Grabar:

![captura de pantalla que muestra cómo grabar contenido en el Reproductor de Windows Media 12](images/wmp12-verify-burn.png)

**Para comprobar que el contenido comprado se puede queman**

1.  Compruebe que el contenido adquirido se compra reproduciendo el CD o DVD después de que se complete la grabación.

2.  Compruebe que el recuento de la grabación se ha decrementado.

    Vaya a la biblioteca y abra los derechos de uso multimedia de una pista comprada que se ha quemando.

    Si el número de veces que se puede grabar una pista es limitado, compruebe que este número disminuye después de que se desanme la pista.

### <a name="transferring-content"></a>Transferencia de contenido

Transferir contenido a otro equipo.

**Para comprobar que el contenido adquirido se puede transferir a otro equipo**

-   Si la tienda permite transferir contenido a otro equipo, transfiera el contenido a al menos dos equipos.

En primer lugar, realice los pasos siguientes para sincronizar con un dispositivo y transferir el contenido adquirido a ese dispositivo y, a continuación, realice los pasos que siguen los pasos iniciales para comprobar que el contenido se transfiere:

> [!Note]  
> Antes de transferir una pista comprada, anote su recuento de sincronización para poder comprobar más adelante si el recuento disminuye después de transferir la pista.

 

1.  Conectar un dispositivo con un reloj seguro. Algunos ejemplos son los dispositivos que usan Windows DRM multimedia para dispositivos portátiles, como un centro multimedia portátil como iRiver H10, Creative Zen, entre otros.
2.  En Reproductor de Windows Media, haga clic en **la pestaña** Sincronizar.
3.  Arrastre el contenido de la biblioteca al **área de lista** Sincronización de la **pestaña** Sincronizar.
4.  Haga clic en **el botón Iniciar sincronización.**

En la captura de pantalla siguiente se muestra  la pista 1 en el área **de** lista Sincronización y el botón Iniciar sincronización Reproductor de Windows Media 11:

![captura de pantalla que muestra cómo transferir contenido en el Reproductor de Windows Media 11](images/wmp11-verify-transfer.png)

En la captura de pantalla siguiente se muestra  la pista 1 en el área **de** lista Sincronización y se muestra el botón Iniciar sincronización Reproductor de Windows Media 12:

![captura de pantalla que muestra cómo transferir contenido en el Reproductor de Windows Media 12](images/wmp12-verify-transfer.png)

**Para comprobar que el contenido comprado se puede transferir a otro dispositivo**

1.  Compruebe que el contenido adquirido se transfiere al dispositivo reproduciendo el contenido en el dispositivo. El contenido transferido también debe tener los metadatos adecuados.

2.  Compruebe que el recuento de sincronización se ha decrementado.

    Vaya a la biblioteca y abra los derechos de uso multimedia de una pista transferida.

    Si el número de veces que se puede sincronizar una pista es limitado, compruebe que este número disminuye cuando se transfiere la pista.

## <a name="store-features"></a>Características de la tienda

En las secciones siguientes se describe cómo probar varias características de una tienda en línea abordada.

### <a name="managing-an-account"></a>Administración de una cuenta

Inicie sesión con una cuenta que haya realizado algunas compras y abra el historial de compras.

**Para comprobar el historial de compras**

-   Compruebe que el historial de compras realiza un seguimiento de las compras anteriores.

Si el tipo de tienda o cuenta admite esta característica, intente restaurar una compra eliminada.

**Para comprobar que se pueden volver a adquirir las compras anteriores**

-   Compruebe que se puede restaurar una compra anterior.

Si el almacén admite el uso de varios equipos con la cuenta, compruebe cualquier funcionalidad que esta característica proporciona.

**Para comprobar la administración de varios equipos con una sola cuenta**

-   Compruebe la funcionalidad del almacén para administrar varios equipos.

### <a name="managing-a-store-specific-account"></a>Administración de una cuenta Store-Specific cliente

Es posible que el almacén no tenga tipos de cuenta, restricciones o contenido típicos. Por ejemplo, una tienda que alquila vídeo de streaming necesitará alguna interfaz de usuario para mostrar los alquileres activos y esa interfaz de usuario tendría que probarse.

> [!Note]  
> Aunque Microsoft no puede certificar la funcionalidad de la cuenta específica de la tienda, para garantizar una buena experiencia del cliente, debe probar esa funcionalidad.

 

### <a name="managing-the-info-center"></a>Administración del Centro de información

En primer lugar, realice los pasos siguientes para prepararse para probar el estado predeterminado y, a continuación, realice el siguiente paso que sigue los pasos iniciales para comprobar que el Centro de información está desactivado de forma predeterminada:

1.  Reproducir contenido de la tienda.
2.  Cambie al modo De reproducción ahora. En Windows XP o Windows Vista con Reproductor de Windows Media 11, haga clic en la **pestaña Reproducción** ahora. En Windows 7 con Reproductor de Windows Media 12, haga clic en el botón Cambiar a reproducción **ahora** en la esquina inferior derecha.

**Para comprobar que el Centro de información está desactivado de forma predeterminada**

-   Compruebe que el Centro de información está desactivado de forma predeterminada.

Si la tienda ofrece una vista del Centro de información, reproduce contenido de la tienda y, mientras se reproduce el contenido, cambia al modo Reproducción ahora y activa el Centro de información.

En Windows XP o Windows Vista con Reproductor de Windows Media 11, haga clic con el botón derecho en la ventana que se reproduce ahora y, a continuación, en el menú contextual, seleccione Vista del Centro de **información**.

En la captura de pantalla siguiente se muestra el menú contextual Reproductor de Windows Media 11:

![captura de pantalla que muestra cómo acceder al centro de información de una tienda en el Reproductor de Windows Media 11](images/wmp11-info-center.png)

En Windows 7 con Reproductor de Windows Media 12, haga clic con el botón derecho en la ventana que se reproduce ahora, en el menú contextual seleccione Visualizaciones y, a continuación, haga clic en Vista **del Centro** de información .

En la captura de pantalla siguiente se muestra el menú contextual Reproductor de Windows Media 12:

![captura de pantalla que muestra cómo acceder al centro de información de una tienda en el Reproductor de Windows Media 12](images/wmp12-info-center.png)

**Para comprobar que el Centro de información es funcional**

-   Compruebe que el Centro de información muestra información multimedia en el área que se está reproduciendo ahora. En la captura de pantalla siguiente se muestra un ejemplo de dicha información multimedia:

    ![captura de pantalla que muestra la funcionalidad del centro de información de una tienda](images/media-information.png)

Si aparecen vínculos de compra u otros vínculos en la página, haga clic en ellos.

**Para comprobar los vínculos en la vista Del Centro de información**

-   Compruebe que los vínculos muestran el almacén.

    El Reproductor de Windows Media debe cambiar al almacén en su biblioteca.

## <a name="store-interaction"></a>Interacción del almacén

En las secciones siguientes se describe cómo probar la interacción entre los otros almacenes y el almacén que está probando.

### <a name="yielding-to-the-active-store"></a>Yielding to the Active Store

Cambie a un almacén que no sea el almacén que se está probando.

**Para comprobar el rendimiento en el almacén activo**

-   Compruebe que el almacén probado se produce en el almacén activo.

### <a name="preventing-the-tested-store-from-taking-over-the-active-store"></a>Impedir que el almacén probado tome el control del almacén activo

-   Con otro almacén seleccionado, cierre Reproductor de Windows Media y reinicie el equipo.
-   Inicie Reproductor de Windows Media.

**Para comprobar que el almacén probado no toma el control**

-   Compruebe que aparece el almacén activo más reciente y que el almacén probado no aparece.

### <a name="accessing-a-store-in-high-contrast-mode"></a>Acceso a un almacén en High-Contrast automático

En primer lugar, para habilitar el modo de contraste alto, presione MAYÚS IZQUIERDA+ALT IZQUIERDA+IMPRIMIR PANTALLA y, a continuación, realice los pasos siguientes para comprobar la accesibilidad de contraste alto:

**Para comprobar que el almacén es accesible en modo de contraste alto**

1.  Compruebe que la interfaz de usuario de inicio de sesión está intacta y funciona.
2.  Compruebe que todas las ventanas y cuadros de diálogo aparecen correctamente.
3.  Medios de compra. Compruebe que los botones de compra y descarga, los administradores de descarga, la información de precios, entre otros, están visibles.
4.  Compruebe que puede transmitir, grabar y sincronizar.
5.  Busque texto recortado y elementos de la interfaz de usuario, texto que no sea legible y otros defectos visibles.

### <a name="securing-a-store"></a>Protección de un almacén

Realice los pasos siguientes para comprobar la seguridad de la cuenta:

**Para comprobar la seguridad de la cuenta**

1.  Escriba la información de la cuenta con formato anterior en la página de inicio de sesión y en el cuadro de diálogo y compruebe que el almacén la rechaza.
2.  Inicie sesión, vea la página de la cuenta y cerrar la sesión.
3.  Haga clic en el botón Atrás Reproductor de Windows Media y compruebe que no ve la información de la cuenta de usuario anterior.

 

 




