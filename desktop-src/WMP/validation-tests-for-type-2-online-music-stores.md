---
title: Pruebas de validación para las tiendas en línea del tipo de incorporación 2
description: En este tema se describen las pruebas que Microsoft realizará para validar la tienda en línea de tipo 2. Microsoft requiere que ejecute estas pruebas antes de enviar una versión candidata para lanzamiento. La tienda en línea debe superar correctamente estas pruebas para que se publiquen.
ms.assetid: 1da51772-9711-4913-b05d-830fabe49da2
keywords:
- Windows Media Player tiendas en línea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beefd0945f9d1a9ae61e61f8be74beada1695baf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418753"
---
# <a name="validation-tests-for-on-boarding-type-2-online-stores"></a>Pruebas de validación para las tiendas en línea del tipo de incorporación 2

En este tema se describen las pruebas que Microsoft realizará para validar la tienda en línea de tipo 2. Microsoft requiere que ejecute estas pruebas antes de enviar una versión candidata para lanzamiento. La tienda en línea debe superar correctamente estas pruebas para que se publiquen.

> [!Note]  
> Si su almacén es de tipo 1 en lugar de tipo 2, puede usar este tema como guía para comprender el ámbito de las pruebas de certificación que se trata para los almacenes de tipo 1. Para obtener el conjunto completo de pruebas para los almacenes de tipo 1, póngase en contacto con [soporte técnico de Microsoft](https://support.microsoft.com/ph/7763#tab0).

 

En este tema se incluyen las siguientes secciones.

-   [Lista de comprobación de prueba](#test-checklist)
    -   [Preparación de prueba superada](#test-pass-preparation)
-   [Entorno de prueba](#test-environment)
-   [Instalación y configuración](#configuration-and-setup)
    -   [Configuración de una máquina de pruebas](#setting-up-a-test-machine)
    -   [Configuración de un almacén](#setting-up-a-store)
    -   [Creación de una cuenta](#creating-an-account)
    -   [Configuración del almacenamiento en caché de credenciales](#setting-up-credential-caching)
-   [Adquisición de contenido](#content-acquisition)
    -   [Contenido de streaming](#streaming-content)
    -   [Obtener contenido](#obtaining-content)
    -   [Grabar contenido](#burning-content)
    -   [Transferir contenido](#transferring-content)
-   [Almacenar características](#store-features)
    -   [Administrar una cuenta](#managing-an-account)
    -   [Administrar el centro de información](#managing-the-info-center)
-   [Interacción de la tienda](#store-interaction)
    -   [Producir en el almacén activo](#yielding-to-the-active-store)
    -   [Impedir que el almacén probado tome el control en el almacén activo](#preventing-the-tested-store-from-taking-over-the-active-store)
    -   [Acceso a un almacén en modo de High-Contrast](#accessing-a-store-in-high-contrast-mode)
    -   [Protección de un almacén](#securing-a-store)

## <a name="test-checklist"></a>Lista de comprobación de prueba

Use la lista de comprobación de la siguiente tabla para validar la tienda en línea de tipo 2 que desea incorporar a la placa.



Prueba

Windows XP

Windows Vista

Windows 7

Resultado (Pass/Fail/no aplicable)

32

64

32

64

32

64

1. Compruebe que el software se instala.

2. Compruebe que se desinstala el software.

3. Compruebe que el software no se ejecuta en la bandeja.

4. Compruebe que funciona la pestaña almacén.

5. Compruebe que el almacén tiene una opción para crear una cuenta nueva.

6. Compruebe que la cuenta creada puede iniciar sesión.

7. Compruebe que el almacén tiene una opción para guardar la información de usuario.

8. Compruebe que el almacenamiento en caché de credenciales está presente y en funcionamiento.

9. Compruebe que al usuario se le piden las credenciales si no están almacenadas en caché.

10. Compruebe que todos los tipos disponibles de flujo de contenido.

11. Compruebe que el contenido se reproduce en Microsoft Windows Media Player.

12. Compruebe que el precio calculado es correcto.

13. Compruebe que el contenido adquirido se descarga en la biblioteca.

14. Compruebe que se han descargado los metadatos de la compra.

15. Compruebe que los derechos de uso de medios sean correctos para la compra.

16. Compruebe que el contenido adquirido puede reproducirse.

17. Compruebe que al hacer  clic en **el botón comprar o comprar,** se cambia a la tienda.

18. Compruebe que se ha descargado el contenido adquirido.

19. Compruebe que se puede grabar el contenido adquirido.

20. Compruebe que se reduce el número de grabaciones.

21. Compruebe que el contenido se puede transferir a otro equipo.

22. Compruebe que el contenido se transfiere a un dispositivo.

23. Compruebe que se reduce el número de sincronizaciones.

24. Compruebe que el historial de compras realiza un seguimiento de las compras anteriores.

25. Compruebe que se puede restaurar una compra anterior.

26. Compruebe la funcionalidad de un almacén para administrar varios equipos.

27. Compruebe que el centro de información está desactivado de forma predeterminada.

28. Compruebe que el centro de información tiene información multimedia en el área de reproducción en curso.

29. Compruebe que los vínculos naveguen a la tienda.

30. Compruebe que el almacén probado produce el almacén activo.

31. Compruebe que el almacén probado no asuma el almacén actual.

32. Compruebe que el almacén es accesible en el modo de alto contraste.

33. Compruebe que el almacén es seguro.



 

### <a name="test-pass-preparation"></a>Preparación de prueba superada

Antes de ejecutar una prueba superada, debe asegurarse de que el almacén y las cuentas de prueba están listos para las pruebas. Debe determinar la siguiente información antes de que se inicie el paso. Si puede determinar la información de algunos días antes de que se supere la prueba, el paso se ejecutará de forma más eficaz.

-   Determine la siguiente información acerca de las cuentas de prueba suministradas por el almacén:
    -   Las cuentas y las contraseñas funcionan para permitir que un usuario inicie sesión
    -   Las cuentas se financian correctamente y de forma adecuada para cada tipo de modo de negocio que ofrece la tienda
    -   Las cuentas son válidas para todas las configuraciones regionales que se van a probar o existen cuentas para cada configuración regional si las cuentas no pueden cruzar configuraciones regionales.
-   Determine las configuraciones regionales que se van a probar.
-   Determine los idiomas que se van a probar.
-   Determine la siguiente información sobre el entorno de prueba:

    -   Tiendas en directo que funcionan con Windows XP, Windows Vista y Windows 7
    -   El almacén no activo que se va a probar
    -   Compruebe que el almacén no activo que se va a probar es visible en todas las versiones del sistema operativo y en todas las versiones de la plataforma Windows Media Player.

-   Determine la siguiente información sobre el almacén que se va a probar:

    -   Nombre de almacén
    -   Etiqueta y gráficos del logotipo de la pestaña del almacén esperado
    -   ¿Está el almacén activo para todas las versiones de sistema operativo?
    -   ¿Se trata de una nueva versión del almacén en pruebas?
    -   ¿El almacén en prueba es de tipo 1 o de tipo 2?
    -   ¿Ha cambiado el tipo de almacén?

-   Determine en qué versiones y plataformas de sistema operativo planea probar la tienda.
-   Determine que el instalador y el complemento funcionan en todas las plataformas y versiones de sistema operativo que se van a probar.
-   Determine si es necesario un documento de navegación.
-   Determine la siguiente información sobre los medios que ofrece el almacén:

    -   Formatos
    -   ¿Se requiere software de propiedad?
    -   ¿Debe probar todos los tipos de medios o solo un subconjunto de tipos de medios?

-   Determine la siguiente información sobre los derechos de uso de medios:

    -   ¿Los medios de almacenamiento tienen protección de contenido?
    -   Si es así, determine el tipo de protección de contenido que tienen los medios.
    -   Si es así, determine el comportamiento protegido esperado.
    -   ¿Los derechos de uso de medios incluyen el uso compartido de equipos a equipos?
    -   Derechos de sincronización
    -   Los derechos de grabación
    -   Los derechos de reproducción
    -   Fechas de expiración, si las hay.

-   Determine si dispone de medios suficientes (un catálogo suficientemente grande) para proporcionar un ejemplo significativo.
-   Determine cuál es el paso de la fase: RC 0, cumplimiento, etc.
-   Determine si la prueba superada es un tipo determinado: regresión, humo, etc.

## <a name="test-environment"></a>Entorno de prueba

Debe realizar pruebas en las siguientes configuraciones:

-   Sistemas operativos de Microsoft Windows Media Player 11 en Windows XP con Service Pack 3 (SP3) 32 y 64 bits
-   Sistemas operativos Windows Media Player 11 en Windows Vista 32 y 64 bits (Windows Media Player de 32 bits)
-   Sistemas operativos de Microsoft Windows Media Player 12 en Windows 7 32 y de 64 bits (Windows Media Player de 32 bits)

Aunque debe realizar pruebas en todas las plataformas y versiones de sistema operativo enumeradas, las versiones de 32 bits de Windows Vista y Windows 7 son las versiones de sistema operativo de destino prioritario. Debe probar la instalación de cualquier software en todas las plataformas.

Las capturas de pantalla de este tema usan un almacén ficticio, Proseware, para demostrar el uso de la interfaz de usuario.

## <a name="configuration-and-setup"></a>Instalación y configuración

En las secciones siguientes se describe cómo configurar y configurar las pruebas de validación en una tienda en línea de tipo 2.

### <a name="setting-up-a-test-machine"></a>Configuración de una máquina de pruebas

Realice los pasos siguientes para configurar un equipo de pruebas:

1.  Señale el equipo de prueba a los servidores de prueba de contenido agregando una clave del registro específica del almacén.
2.  Establezca los valores del cuadro de diálogo Configuración **regional y de idioma** en la configuración regional y de idioma adecuada. Para establecer el idioma, seleccione la pestaña **formatos** y, a continuación, seleccione el idioma en el cuadro combinado **formato actual** . Para establecer la región, seleccione la pestaña **Ubicación** y, a continuación, seleccione la región en el cuadro combinado **ubicación actual** . Además, en el caso de los almacenes que requieran la instalación de un complemento o un software personalizado específico del almacén, es posible que deba cambiar la configuración regional del sistema al idioma de la configuración regional del almacén para facilitar la instalación. El instalador de software debe ser compatible con caracteres de byte único y doble y debe ejecutarse en cualquier configuración regional. Debe probar la configuración regional nativa. Para establecer la configuración regional nativa, abra el cuadro de diálogo **región e idioma** , seleccione la pestaña **administrativo** y, a continuación, haga clic en el botón **Cambiar configuración regional del sistema** como se muestra en la siguiente captura de pantalla. Al hacer clic en este botón, se muestra el cuadro **de diálogo Configuración de región e idioma** . El cuadro combinado actual de la **configuración regional del sistema** de ese cuadro de diálogo cambia la configuración regional del sistema.

    En las siguientes capturas de pantalla se muestran las pestañas en las que puede establecer la región y el idioma:

    ![captura de pantalla del cuadro de diálogo Opciones regionales y de idioma](images/reg-lang-opt.png)

    ![captura de pantalla que muestra cómo cambiar la configuración regional actual del sistema](images/reg-lang-settings.png)

3.  Desactive la vista del centro de información de un almacén estableciendo Windows Media Player para reproducir una visualización. La diferencia principal entre las plataformas es que en Windows Media Player 11, para empezar, haga clic en **reproducción** en curso, mientras que en Windows Media Player 12, haga clic con el botón secundario en la ventana principal.

    En la captura de pantalla siguiente se muestra la secuencia de opciones de menú que reproduce una visualización en Windows Media Player 11:

    ![captura de pantalla que muestra cómo reproducir una visualización en el reproductor de Windows Media 11](images/wmp11-visual.png)

    En la captura de pantalla siguiente se muestra la secuencia de opciones de menú que reproduce una visualización en Windows Media Player 12:

    ![captura de pantalla que muestra cómo reproducir una visualización en el reproductor de Windows Media 12](images/wmp12-visual.png)

### <a name="setting-up-a-store"></a>Configuración de un almacén

En primer lugar, realice los pasos siguientes para configurar un almacén y, a continuación, siga los pasos iniciales para comprobar la configuración del almacén:

1.  Inicie Windows Media Player y espere unos segundos para adquirir el archivo de AllServices.xml más reciente.
2.  En Windows XP y Windows Vista, para seleccionar una tienda en línea, primero haga clic en la pestaña que se divide entre la vista de la guía multimedia y la vista de tiendas en línea. A continuación, en el menú, haga clic en **examinar todas las tiendas en línea** y seleccione la tienda haciendo clic en su icono en la lista de tiendas. En Windows 7, haga clic en el botón del panel de navegación biblioteca que se divide entre el botón **guía multimedia** y el botón **tiendas en línea** . A continuación, en el menú, haga clic en **examinar todas las tiendas en línea** y seleccione la tienda haciendo clic en su icono en la lista de tiendas.

    En la captura de pantalla siguiente se muestra cómo seleccionar una tienda en línea en Windows Media Player 11:

    ![captura de pantalla que muestra cómo seleccionar una tienda en línea en el reproductor de Windows Media 11](images/wmp11-set-store.png)

    En la captura de pantalla siguiente se muestra cómo seleccionar una tienda en línea en Windows Media Player 12:

    ![captura de pantalla que muestra cómo seleccionar una tienda en línea en el reproductor de Windows Media 12](images/wmp12-set-store.png)

3.  Siga las instrucciones de la tienda para instalar cualquier software adicional que sea necesario para usar el almacén.

**Para comprobar la configuración del almacén**

1.  Compruebe que el software se instala.

    Compruebe que el complemento OCX o cualquier otro software de la tienda se descargue e instale sin errores.

2.  Compruebe que el software se desinstala.

    Compruebe que en el panel de control, en el elemento **programas y características** , aparece el software que instala el almacén en la lista **desinstalar o cambiar un programa** , y compruebe que puede desinstalarlo de esta lista sin errores.

3.  Compruebe que el software no se ejecuta en la bandeja del sistema.

    Compruebe que ningún software del almacén agrega iconos al área de notificación del programa (en la barra de tareas situada a la izquierda del reloj) antes del consentimiento del cliente para descargar el software de la tienda.

    La experiencia de tienda básica no debe requerir la instalación de software adicional. Debe haber disponible una experiencia multimedia básica, como la transmisión por secuencias de multimedia. Algunos almacenes instalan software adicional, como los administradores de descargas para una experiencia multimedia Premier. Estos almacenes pueden tener iconos en la bandeja del sistema si los iconos representan aplicaciones independientes de Windows Media Player.

4.  Compruebe que funciona la pestaña almacén.

    Compruebe que la pestaña almacén cambia para indicar el almacén seleccionado.

    En Windows XP y Windows Vista con Windows Media Player 11, compruebe que el nombre del almacén y el icono están visibles en el fondo de Windows Media Player 11 oscuro.

    En Windows 7 con Windows Media Player 12, compruebe que el nombre del almacén y el icono están visibles en el panel de navegación biblioteca, en el menú contextual del selector de servicio.

    Compruebe que la tienda aparece en la parte superior de la lista de selección de almacén en el menú.

    > [!Note]  
    > No habrá ninguna opción de **menú Agregar servicio actual a** si el almacén de tipo 2 es el almacén destacado (predeterminado) para la región.

     

    En la captura de pantalla siguiente se muestra el menú que aparece al hacer clic en la pestaña en la esquina superior derecha de Windows Media Player 11:

    ![captura de pantalla que muestra la pestaña de almacenamiento en el reproductor de Windows Media 11](images/wmp11-verify-store.png)

    En la captura de pantalla siguiente se muestra el menú que aparece al hacer clic en el botón de expansión situado en la esquina inferior izquierda de Windows Media Player 12:

    ![captura de pantalla que muestra la pestaña de almacenamiento en el reproductor de Windows Media 12](images/wmp12-verify-store.png)

### <a name="creating-an-account"></a>Creación de una cuenta

**Para comprobar la configuración de la cuenta**

1.  Compruebe que la tienda tiene una opción para crear una cuenta nueva y, a continuación, siga las instrucciones de la tienda para crear una cuenta nueva.

    En la siguiente captura de pantalla se resalta un botón **crear nueva cuenta** , como podría aparecer en Windows Media Player 11:

    ![captura de pantalla que muestra cómo comprobar la configuración de la cuenta del reproductor de Windows Media 11](images/wmp11-verify-account.png)

    En la siguiente captura de pantalla se resalta un botón **crear nueva cuenta** , como podría aparecer en Windows Media Player 12:

    ![captura de pantalla que muestra cómo comprobar la configuración de la cuenta del reproductor de Windows Media 12](images/wmp12-verify-account.png)

2.  Compruebe que puede iniciar sesión en la cuenta que ha creado.

### <a name="setting-up-credential-caching"></a>Configuración del almacenamiento en caché de credenciales

En primer lugar, realice los pasos siguientes para configurar el almacenamiento en caché de las credenciales y, a continuación, siga los pasos iniciales para comprobar la configuración del almacenamiento en caché de credenciales:

1.  En la página de inicio de sesión, escriba las credenciales y seleccione la opción para guardar la información de usuario.
2.  Compruebe que la página de inicio de sesión tiene una casilla que permite al usuario almacenar en caché las credenciales.
3.  El almacenamiento en caché opcional de credenciales es un punto de seguridad importante. El almacenamiento en caché automático de credenciales puede exponer información de identificación personal de los usuarios que inician sesión en un equipo público o compartido. Debe proteger la información del cliente ofreciendo una casilla que representa el almacenamiento en caché opcional.

**Para comprobar el almacenamiento en caché de credenciales**

1.  Compruebe que la tienda tiene una casilla para la opción **guardar mi información de usuario** .

    1.  Cierre Windows Media Player.
    2.  Vuelva a abrir Windows Media Player e intente descargar el contenido.

2.  Compruebe que el almacenamiento en caché de credenciales está presente y en funcionamiento.

    1.  Cierre la sesión del almacén.
    2.  Cierre Windows Media Player.
    3.  Vuelva a abrir Windows Media Player e intente descargar el contenido.

3.  Compruebe que al usuario se le piden las credenciales si no están almacenadas en caché.

    Después de cerrar la sesión y tratar de usar el almacén, se le pedirán las credenciales al cliente.

## <a name="content-acquisition"></a>Adquisición de contenido

En esta sección se describen las distintas formas de adquirir contenido y de comprobar que se ha adquirido dicho contenido.

### <a name="streaming-content"></a>Contenido de streaming

Transmita todos los tipos de contenido disponibles desde el almacén. Por ejemplo, transmisión por secuencias de radio, vídeo, audio y versiones preliminares.

**Para comprobar el contenido de streaming**

1.  Compruebe que todos los tipos disponibles de flujo de contenido.

2.  Compruebe que el contenido se reproduce en Windows Media Player y no en otro reproductor o control.

### <a name="obtaining-content"></a>Obtener contenido

En primer lugar, realice los pasos siguientes para adquirir contenido y, a continuación, siga los pasos que se indican a continuación para comprobar la compra y comprobar que el contenido se ha descargado:

1.  Inicie Windows Media Player.
2.  Inicie sesión en la cuenta de prueba.
3.  Navegue hasta el contenido que desea comprar.
4.  Siga el procedimiento específico del almacén para comprar contenido.

**Para comprobar el contenido comprado y descargado**

1.  Compruebe que el precio calculado es correcto.

    Compruebe que el precio es correcto, especialmente cuando compra varios fragmentos de contenido a la vez, y compruebe que la información de saldo de la cuenta se ha actualizado correctamente después de la compra. Algunos contenidos se pueden adquirir como pistas únicas y solo como álbumes. Compruebe que el precio del álbum no sea mayor que la suma de las pistas individuales.

2.  Compruebe que el contenido adquirido se descarga en la biblioteca.

    Una vez finalizada la descarga, navegue hasta el contenido descargado en la biblioteca de Windows Media Player. El contenido descargado se encuentra en la biblioteca del usuario actual.

    -   En Windows XP y Windows Vista con Windows Media Player 11, el contenido descargado aparece en el panel de navegación de la biblioteca, en dinámica de **biblioteca** y, a continuación, en **canciones**.
    -   En el caso de Windows 7 con Windows Media Player 12, el contenido que se descarga en la biblioteca de Media Player de Windows aparece en el panel de navegación de Windows Media Player bajo **música**.

3.  Compruebe que las descargas de metadatos para la compra.

    Asegúrese de que las siguientes columnas aparecen en la biblioteca de Media Player de Windows (agréguelas si no):

    -   Intérprete del álbum
    -   Title
    -   Título del álbum
    -   Proveedor de contenido
    -   Género

    Se deben rellenar las columnas anteriores. El contenido debe tener carátulas de álbum. Sin embargo, no es necesario carátulas de álbum para pasar las pruebas de validación.

4.  Compruebe que los derechos de uso de medios sean correctos para la compra.

    Para cada pista descargada, haga clic con el botón secundario en la pista y seleccione **propiedades** y, a continuación, seleccione la ficha **derechos de uso de medios** .

    El almacén puede optar por proteger su contenido con derechos de uso de medios o puede optar por no proteger el contenido. La pestaña **derechos de uso de medios** refleja ese estado en la lista de restricciones o indicando que el contenido no está protegido. El almacén debe comunicar su plan más actual para los derechos de uso de medios. Debe comprobar los resultados reales en relación con este comportamiento esperado.

    Las licencias de los derechos multimedia deben entregarse previamente. El cliente no debe ser necesario para reproducir el contenido o pasar por algún otro proceso para obtener la licencia. Debe comparar los derechos de uso de medios específicos con lo que el almacén ha comunicado al cliente según corresponda. Los derechos deben transferirse al menos a otros dos equipos. Los clientes deben poder grabar y sincronizar sus medios.

    En la captura de pantalla siguiente se muestran los derechos de uso de medios de un archivo protegido:

    ![captura de pantalla que muestra los derechos de uso de medios para un archivo protegido](images/media-rights-protected.png)

    Si el contenido no está protegido, la ficha **derechos de uso de medios** indica este hecho.

    En la captura de pantalla siguiente se muestran los derechos de uso de medios de un archivo sin protección:

    ![captura de pantalla que muestra los derechos de uso de medios para un archivo no protegido](images/media-rights-not-protected.png)

5.  Compruebe que el contenido adquirido se reproduzca.

    Compruebe que el contenido descargado se reproduce en Windows Media Player.

    Reproducir cualquier contenido adquirido en la tienda y que resida en la biblioteca local, o bien transmitir una vista previa.

    Realice los pasos siguientes para adquirir contenido en Windows XP y Windows Vista con Windows Media Player 11:

    1.  Haga clic en la pestaña **reproducción en curso** .
    2.  En el panel lista, coloque el puntero del mouse para desplazarse sobre las carátulas de álbum con el fin de mostrar el vínculo **comprar** .
    3.  Haga clic en **comprar**.

    En la captura de pantalla siguiente se muestra la ubicación del vínculo **Buy** en Windows Media Player 11:

    ![captura de pantalla que muestra cómo comprar contenido en el reproductor de Windows Media 11](images/wmp11-verify-buy-play.png)

    Realice los pasos siguientes para comprar contenido en Windows 7 con Windows Media Player 12:

    1.  En el modo de biblioteca, haga clic en la pestaña **reproducir** .
    2.  En la lista de reproducción, en la carátula del álbum, haga clic en **tienda**

    En la captura de pantalla siguiente se muestra cómo comprar contenido en Windows Media Player 12:

    ![captura de pantalla que muestra cómo comprar contenido en el reproductor de Windows Media 12](images/wmp12-verify-buy-play.png)

6.  Compruebe que al hacer clic en **comprar o comprar** cambia a **la tienda.**

    La Media Player de Windows debe cambiar a la tienda en la vista biblioteca y cargar la experiencia de compra de la tienda.

    Después, debe continuar con la compra de la pista.

7.  Compruebe que **después de hacer** clic en comprar o **comprar** , el contenido se descarga.

    Compruebe que los derechos de uso de medios sean adecuados para el contenido adquirido y sus metadatos, y compruebe que el seguimiento se reproduce. En general, este método de compra debe tener los mismos resultados que otros métodos.

### <a name="burning-content"></a>Grabar contenido

En primer lugar, realice los pasos siguientes para grabar contenido adquirido (Copie el contenido adquirido en un CD o DVD grabable) y, a continuación, siga los pasos que se indican a continuación para comprobar que el contenido se grabe:

> [!Note]  
> Antes de grabar una pista comprada, tenga en cuenta su número de grabaciones para que pueda comprobar más adelante si el recuento disminuye después de grabar la pista.

 

1.  Haga clic en la pestaña **grabar** .
2.  Arrastre pistas compradas a la **lista de grabación**.
3.  Haga clic en el botón **iniciar grabación** .

En la captura de pantalla siguiente se muestra la **lista de grabación** en el lado derecho de la pantalla y el botón **iniciar grabación** debajo de la **lista de grabación** en Windows Media Player 11:

![captura de pantalla que muestra cómo grabar contenido en el reproductor de Windows Media 11](images/wmp11-verify-burn.png)

En la captura de pantalla siguiente se muestra cómo aparece la lista de grabación en Windows Media Player 12 después de arrastrar una pista a la lista de grabación y se muestra el botón **iniciar grabación** en la parte superior de la pestaña **grabar** :

![captura de pantalla que muestra cómo grabar contenido en el reproductor de Windows Media 12](images/wmp12-verify-burn.png)

**Para comprobar que se puede grabar el contenido adquirido**

1.  Compruebe que el contenido adquirido se grabe reproduciendo el CD o DVD una vez finalizada la grabación.

2.  Compruebe que se reduce el número de grabaciones.

    Vaya a la biblioteca y abra los derechos de uso de medios para una pista comprada que se grabó.

    Si el número de veces que se puede grabar una pista es limitado, compruebe que este número disminuye después de grabar la pista.

### <a name="transferring-content"></a>Transferir contenido

Transferir contenido a otro equipo.

**Para comprobar que el contenido adquirido se puede transferir a otro equipo**

-   Si el almacén permite transferir contenido a otro equipo, transfiera el contenido a dos equipos como mínimo.

En primer lugar, realice los pasos siguientes para sincronizar con un dispositivo y transferir el contenido adquirido a ese dispositivo y, a continuación, siga los pasos que se indican a continuación para comprobar que el contenido se transfiere:

> [!Note]  
> Antes de transferir una pista comprada, tenga en cuenta su número de sincronizaciones para que pueda comprobar más adelante si el recuento disminuye después de transferir la pista.

 

1.  Conectar un dispositivo con un reloj seguro. Algunos ejemplos son los dispositivos que usan DRM de Windows Media para dispositivos portátiles, como un centro multimedia portátil como iRiver H10, Creative Zen, etc.
2.  En Windows Media Player, haga clic en la pestaña **sincronizar** .
3.  Arrastre el contenido de la biblioteca al área **lista de sincronización** de la pestaña **sincronizar** .
4.  Haga clic en el botón **Iniciar sincronización** .

En la captura de pantalla siguiente se muestra el seguimiento 1 en el área de **lista de sincronización** y se muestra el botón **Iniciar sincronización** en Windows Media Player 11:

![captura de pantalla que muestra cómo transferir contenido en el reproductor de Windows Media 11](images/wmp11-verify-transfer.png)

En la captura de pantalla siguiente se muestra el seguimiento 1 en el área de **lista de sincronización** y se muestra el botón **Iniciar sincronización** en Windows Media Player 12:

![captura de pantalla que muestra cómo transferir contenido en el reproductor de Windows Media 12](images/wmp12-verify-transfer.png)

**Para comprobar que el contenido adquirido se puede transferir a otro dispositivo**

1.  Compruebe que el contenido adquirido se transfiere al dispositivo reproduciendo el contenido en el dispositivo. El contenido transferido también debe tener los metadatos adecuados.

2.  Compruebe que se reduce el número de sincronizaciones.

    Navegue a la biblioteca y abra los derechos de uso de medios para una pista transferida.

    Si el número de veces que se puede sincronizar una pista es limitado, compruebe que este número se reduce cuando se transfiere la pista.

## <a name="store-features"></a>Almacenar características

En las secciones siguientes se describe cómo probar varias características de una tienda en línea incorporada.

### <a name="managing-an-account"></a>Administrar una cuenta

Inicie sesión con una cuenta que haya realizado algunas compras y abra el historial de compras.

**Para comprobar el historial de compras**

-   Compruebe que el historial de compras realiza un seguimiento de las compras anteriores.

Si el tipo de almacén o cuenta es compatible con esta característica, intente restaurar una compra eliminada.

**Para comprobar que las compras anteriores se pueden readquirir**

-   Compruebe que se puede restaurar una compra anterior.

Si el almacén admite el uso de varios equipos con la cuenta, compruebe las funciones que proporciona esta característica.

**Para comprobar la administración de varios equipos con una sola cuenta**

-   Compruebe la funcionalidad del almacén para administrar varios equipos.

### <a name="managing-a-store-specific-account"></a>Administración de una cuenta de Store-Specific

Es posible que el almacén no tenga tipos de cuenta, restricciones o contenido típicos. Por ejemplo, un almacén que alquila el vídeo de streaming necesitará alguna interfaz de usuario para mostrar los alquileres activos y la interfaz de usuario se debe probar.

> [!Note]  
> Aunque Microsoft no puede certificar la funcionalidad de la cuenta específica del almacén, para garantizar una buena experiencia del cliente, debe probar esa funcionalidad.

 

### <a name="managing-the-info-center"></a>Administrar el centro de información

En primer lugar, realice los pasos siguientes para preparar la prueba del estado predeterminado y, a continuación, realice el siguiente paso que sigue los pasos iniciales para comprobar que el centro de información está desactivado de forma predeterminada:

1.  Reproducir contenido de la tienda.
2.  Cambiar al modo de reproducción en curso. En Windows XP o Windows Vista con Windows Media Player 11, haga clic en la pestaña **reproducción en curso** . En Windows 7 con Windows Media Player 12, haga clic en el botón **cambiar a reproducción en curso** en la esquina inferior derecha.

**Para comprobar que el centro de información está desactivado de forma predeterminada**

-   Compruebe que el centro de información está desactivado de forma predeterminada.

Si el almacén ofrece una vista de centro de información, reproduzca parte del contenido del almacén y mientras se reproduce el contenido, cambie al modo de reproducción en curso y Active info Center.

En Windows XP o Windows Vista con Windows Media Player 11, haga clic con el botón derecho en la ventana de reproducción en curso y, a continuación, en el menú contextual, seleccione **info Center View**.

En la captura de pantalla siguiente se muestra el menú contextual en Windows Media Player 11:

![captura de pantalla que muestra cómo obtener acceso al centro de información de un almacén en el reproductor de Windows Media 11](images/wmp11-info-center.png)

En Windows 7 con Windows Media Player 12, haga clic con el botón derecho en la ventana de reproducción en curso, seleccione **visualizaciones** en el menú contextual y, a continuación, haga clic en **info Center View**.

En la captura de pantalla siguiente se muestra el menú contextual de Windows Media Player 12:

![captura de pantalla que muestra cómo obtener acceso al centro de información de un almacén en el reproductor de Windows Media 12](images/wmp12-info-center.png)

**Para comprobar que el centro de información es funcional**

-   Compruebe que el centro de información muestra información multimedia en el área de reproducción en curso. En la captura de pantalla siguiente se muestra un ejemplo de la información multimedia:

    ![captura de pantalla que muestra la funcionalidad del centro de información de un almacén](images/media-information.png)

Si aparecen vínculos de compra u otros vínculos en la página, haga clic en los vínculos.

**Para comprobar los vínculos en la vista de centro de información**

-   Compruebe que los vínculos muestran el almacén.

    El Media Player de Windows debe cambiar al almacén en su biblioteca.

## <a name="store-interaction"></a>Interacción de la tienda

En las secciones siguientes se describe cómo probar la interacción entre los otros almacenes y el almacén que se está probando.

### <a name="yielding-to-the-active-store"></a>Producir en el almacén activo

Cambie a un almacén que no sea el almacén que se está probando.

**Para comprobar la producción en el almacén activo**

-   Compruebe que el almacén probado produce el almacén activo.

### <a name="preventing-the-tested-store-from-taking-over-the-active-store"></a>Impedir que el almacén probado tome el control en el almacén activo

-   Con otro almacén seleccionado, cierre Windows Media Player y reinicie el equipo.
-   Inicie Windows Media Player.

**Para comprobar que el almacén probado no toma el control**

-   Compruebe que el último almacén activo aparece y que el almacén probado no aparece.

### <a name="accessing-a-store-in-high-contrast-mode"></a>Acceso a un almacén en modo de High-Contrast

En primer lugar, habilite el modo de alto contraste presionando Mayús Izq + izquierda ALT + Impr Pant y, a continuación, realice los pasos siguientes para comprobar la accesibilidad de contraste alto:

**Para comprobar que el almacén es accesible en el modo de alto contraste**

1.  Compruebe que la interfaz de usuario de inicio de sesión está intacta y funciona.
2.  Compruebe que todas las ventanas y cuadros de diálogo aparecen correctamente.
3.  Compra de medios. Compruebe que estén visibles los botones de compra y descarga, los administradores de descargas, la información de precios, etc.
4.  Compruebe que puede transmitir, grabar y sincronizar.
5.  Busque texto recortado y elementos de la interfaz de usuario, texto que no sea legible y otros defectos visibles.

### <a name="securing-a-store"></a>Protección de un almacén

Realice los pasos siguientes para comprobar la seguridad de la cuenta:

**Para comprobar la seguridad de la cuenta**

1.  Escriba la información de cuenta con formato incorrecto en la página de inicio de sesión y el cuadro de diálogo y compruebe que el almacén lo rechaza.
2.  Inicie sesión, vea la página cuenta y cierre la sesión.
3.  Haga clic en el botón atrás de Windows Media Player y compruebe que no ve la información de la cuenta de usuario anterior.

 

 




