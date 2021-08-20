---
title: Programa de aplicaciones de escritorio de Windows
description: Puede obtener datos de telemetría detallados e informes de análisis que le permiten ver cómo funcionan las aplicaciones de escritorio Windows mediante el nuevo programa de aplicaciones de escritorio Windows escritorio.
ms.assetid: F1ED72A5-E1CD-4924-A81B-ED6FAF5E2AA3
ms.topic: article
ms.date: 11/02/2018
ms.openlocfilehash: 90483194654d5656060c57e3ad7593410a08660c2b8fc71bbbe9e42f08f17c45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118105733"
---
# <a name="windows-desktop-application-program"></a>Programa de aplicaciones de escritorio de Windows

Puede obtener datos de telemetría detallados e informes de análisis que le permiten ver cómo funcionan las aplicaciones de escritorio Windows mediante el nuevo programa de aplicaciones de escritorio Windows escritorio.

No hay ningún cargo por acceder a estos [](https://login.microsoftonline.com/common/oauth2/authorize?client_id=4990cffe-04e8-4e8b-808a-1175604b879f&response_mode=form_post&response_type=code+id_token&scope=openid+profile&state=OpenIdConnect.AuthenticationProperties%3deJsPaLaK4fU55nKvN21CjU6FsdJ0aPGfhsjGAZ0HR9bE6rgwHHX4izvRt_w-0VUlIF0ClCya4cVY6Uv4qTAqDrH8LTwFpjFGWVW2BAIJmAAuxBLZGTPS_DYy0wwgvTh1orWTCMvBdlOu_kF8vwNe4mjtk9JRMvYaETyspKrJi-s5Z2K7lKIPqnlFkwSU-aoot-3NxTeQ0wu6_RJ1nf_kLFatEkVAqokDSYTKkpv7zF6gA3YYriMFoC9_f2uxuXpI-STckg&nonce=637177463062493881.YjhiOTZjYTMtOTVhZS00OGM1LWI4MDItNWE5MThjMjA1ZjZmMTAyZDRiMGQtMDJhNC00ZDJmLWFkM2QtM2FjZDJkNjcxYWQy&redirect_uri=https%3a%2f%2fpartner.microsoft.com%2faad%2fauthPostGateway&resource=797f4846-ba00-4fd7-ba43-dac1f8f63013&mkt=en-US) datos todo lo que necesita hacer es registrarse y aceptar el Contrato del programa de aplicaciones de escritorio de Windows y, [a](https://go.microsoft.com/fwlink/?linkid=853677)continuación, cargar un archivo firmado con el mismo certificado que usó para firmar los archivos ejecutables de la aplicación.

## <a name="join-the-windows-desktop-application-program"></a>Unirse al programa Windows desktop

Si su empresa ya tiene una cuenta de **Centro de partners:** inicie sesión en su cuenta de Centro de partners (con la cuenta  Microsoft asociada con  el propietario de la cuenta) y vaya a la página Programas (ya sea en Configuración de la cuenta o seleccionando Todo en el menú de navegación izquierdo).  En **Windows Programa de aplicaciones de escritorio**, haga clic **Introducción** para unirse al programa sin costo adicional. Si tiene un inquilino Azure AD asociado a su cuenta de Centro de partners, los usuarios que haya agregado podrán acceder al programa Windows Aplicación de escritorio. Próximamente, le permitiremos establecer un acceso más granular para este programa.

> [!Tip]  
> Si su empresa tiene una Centro de partners, pero no tiene acceso a ella, pida al administrador que le [agregue como usuario](/windows/uwp/publish/add-users-groups-and-azure-ad-applications). Tenga en cuenta que solo el propietario de la cuenta puede unirse al Windows aplicación de escritorio.

 

**Si su empresa no tiene una** cuenta de Centro de partners : puede registrarse para obtener el programa Windows aplicación de [escritorio](https://login.microsoftonline.com/common/oauth2/authorize?client_id=4990cffe-04e8-4e8b-808a-1175604b879f&response_mode=form_post&response_type=code+id_token&scope=openid+profile&state=OpenIdConnect.AuthenticationProperties%3dWc5R_wIKVD0EbOy2UUxS0_0GQJnIAbD-eisMn7Gb4cJL18fRdelvbtj5_R0zoGlsebcnAxIvwKS5kx4Ma4mLMbU4l9ULsE9ajiZU4wtchLJXyJGsPCjCBUNV7TY1SzwXAI-LepSoXkqa8xSywVb7JZ3Xed-Lcw-kwEShFOwt0SdSdc1nNevHbPOhotOeFQcqbo0HESVYXk6pZORJ_OYimG99onp_zSTyludOvvaTd9GYKUgX9exCU5IHReP7MzJDHOgqTg&nonce=637177463071243612.NDU4MjE2ZTMtNmVkMi00YWNiLWEzZGEtMjYyNDRkODI0M2FmOTM3MmE1NzgtMzQ1OC00M2ZkLWJhMDktYzI4YTNhNzdiYTk0&redirect_uri=https%3a%2f%2fpartner.microsoft.com%2faad%2fauthPostGateway&resource=797f4846-ba00-4fd7-ba43-dac1f8f63013&mkt=en-US) directamente sin costo alguno. Próximamente, proporcionaremos la opción de asociar un inquilino de [Azure AD a](/windows/uwp/publish/add-users-groups-and-azure-ad-applications) su cuenta para que otras personas de su empresa también puedan iniciar sesión.

## <a name="add-your-desktop-applications"></a>Adición de aplicaciones de escritorio

Una vez que se haya unido al programa, deberá agregar las aplicaciones de escritorio de Windows al panel para que podamos empezar a mostrar los informes de análisis.

Usamos la firma de código para establecer la identidad de su empresa y recuperar el análisis de las aplicaciones que publica.

Le proporcionaremos un archivo y le pediremos que lo firme con los mismos certificados de firma de código válidos, no expirados y no revocados que usa para firmar las aplicaciones de escritorio. Después, cargará ese archivo firmado en el panel. Esto nos permite saber que las aplicaciones de escritorio firmadas con el mismo certificado pertenecen a su cuenta. No usamos la información del certificado para ningún otro propósito.

> [!Important]  
> No es necesario repetir este proceso si publica una nueva aplicación de escritorio. Una vez que haya cargado el archivo firmado, identificaremos automáticamente las nuevas aplicaciones que estén firmadas con el mismo certificado y recuperaremos automáticamente el análisis de esos productos. Tampoco es necesario distribuir el archivo proporcionado dentro de las aplicaciones ni enviar ningún tipo de asignación para los productos.

 

**Para agregar una o varias aplicaciones de escritorio**

1.  En el panel, seleccione **Agregar aplicaciones de escritorio.**
2.  En la página siguiente, descargue el archivo que se puede firmar seleccionando **Descargar** el archivo y, a continuación, guarde el archivo en el equipo.
3.  Firme el archivo que acaba de descargar con el mismo certificado de firma de código que usa para autenticar las aplicaciones de escritorio. Puede usar SignTool.exe (disponible en Microsoft Visual Studio y como parte del [SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk)de Windows ) para firmar este archivo. A continuación se describen más detalles sobre este proceso.
4.  Upload el archivo que acaba de firmar arrastrándolo al campo (o haga clic para examinar los archivos).
5.  Seleccione **Enviar** para completar el proceso.

![pasos para agregar aplicaciones de escritorio](images/uploadcert.png)

Si usa más de un certificado de firma de código, puede repetir los pasos anteriores para cada uno de los certificados. Puede descargar, firmar y cargar un archivo para cada certificado actual que use para firmar las aplicaciones. Sin embargo, solo puede usar un certificado por cada archivo descargado.

Después de completar estos pasos, identificaremos qué aplicaciones Windows escritorio están firmadas con el mismo certificado que usó para firmar el archivo. En la mayoría de los casos, comenzaremos a mostrar los informes analíticos en un plazo de 48 horas, aunque en ocasiones pueden tardar un poco más.

## <a name="use-signtoolexe-to-sign-the-downloaded-file"></a>Uso signtool.exe para firmar el archivo descargado

Microsoft proporciona una herramienta para firmar archivos, SignTool.exe, con Visual Studio y en el [SDK Windows .](https://developer.microsoft.com/windows/downloads/windows-10-sdk) Puede usar esta herramienta para realizar y comprobar el proceso de firma de código. Hay más información SignTool.exe disponible [aquí.](/dotnet/framework/tools/signtool-exe)

Estas son dos de las formas más comunes de usar esta herramienta para firmar el archivo que se puede firmar.

-   Si tiene acceso al certificado de firma de código como un archivo de [Exchange personal (PFX):](/windows-hardware/drivers/install/personal-information-exchange---pfx--files)

    ``` syntax
    signtool sign /f MyCert.pfx /p MyCertPassword /v SignableFile.bin
    ```

    ![Captura de pantalla que muestra una ventana del símbolo del sistema que muestra el comando "signtool sign /f MyCert.pfx /p MyCertPassword /v SignableFile.bin".](images/signtool2.png)

-   Si el certificado de firma de código está disponible en el almacén de certificados local:

    ``` syntax
    Signtool sign /v /s MY /n CertSubjectName SignableFile.bin
    ```

    ![ventana del símbolo del sistema que muestra este comando](images/signtool.png)

Después de firmar el archivo, puede comprobar que se ha firmado correctamente con un certificado válido con lo siguiente:

``` syntax
signtool verify /a SignableFile.bin
```

## <a name="viewing-your-analytic-data"></a>Visualización de los datos analíticos

Una vez cargados los archivos firmados y hemos identificado las aplicaciones de escritorio, el panel mostrará información general de las aplicaciones junto con métricas clave.

Nuestros datos de telemetría mostrarán información de estado, como bloqueos, para cada aplicación asociada al certificado. El panel mostrará información general de las aplicaciones junto con métricas clave. Puede seleccionar cualquier aplicación para ver su [informe](#health-report)de mantenimiento, el informe De instalación y el Informe [de bloques](#application-blocks-report) en el panel. [](#installs-report) También puede recuperar [datos analíticos mediante programación mediante la API Microsoft Store analytics](#retrieve-analytic-data-using-the-microsoft-store-analytics-api).

> [!Note]  
> Si detectamos que los metadatos de una aplicación se han actualizado para usar un nuevo nombre, comenzaremos a notificar nuevos datos con el nuevo nombre. Los datos históricos asociados con el nombre antiguo se conservarán durante 30 días.
> 
> Analytics no estará disponible para una aplicación hasta que se haya instalado en al menos 100 dispositivos.


### <a name="health-report"></a>Informe de estado

El **informe** De mantenimiento le permite obtener datos relacionados con el rendimiento y la calidad de la aplicación, incluidos bloqueos y eventos que no responde. Si procede, puede ver los seguimientos de la pila o los archivos CAB para su posterior depuración.

![informe de estado: programa de aplicación de escritorio de Windows](images/health.png)

Puede filtrar los datos de varias maneras, lo que le permite:

-   Ver un resumen de todos los tipos de error, ordenados por número de aciertos
-   Explore en profundidad un error determinado y descargue los seguimientos de la pila para depurar el problema con mayor rapidez.
-   Comparar una nueva versión de la aplicación con las versiones anteriores
-   Ver los datos de mantenimiento agregados o por región, lo que le permite aislar los problemas específicos de una región.
-   Comparar el rendimiento de las aplicaciones de escritorio en Windows versiones anteriores o en una versión específica, como la versión Windows 10 más reciente
-   Visualización de la información de mantenimiento de un archivo ejecutable determinado incluido en la aplicación

Seleccione **Upload símbolos en** la parte superior de la tabla **Errores** para cargar un archivo .zip que contenga los archivos de símbolos de [la aplicación.](/windows-hardware/drivers/debugger/symbols-and-symbol-files) Estos archivos de símbolos se indexarán y usarán para generar seguimientos de pila más precisos. Los tipos de archivo de símbolos .zip deben ser .pdb, .dll o .exe. Después de cargar correctamente el .zip, debería ver menos **! Valores** desconocidos para nuevos errores en la lista de errores de la aplicación en aproximadamente 5 días.

### <a name="installs-report"></a>Instala el informe

El **informe Installs** (Instala) le permite ver el número de dispositivos en los que se instaló una aplicación durante un día determinado y el número medio de dispositivos en los que se instaló cada versión de la aplicación en los últimos 30 días.

Puede filtrar los datos de varias maneras, lo que le permite:

-   Ver un resumen de las instalaciones, ordenado por popularidad
-   Comparar una nueva versión de la aplicación con las versiones anteriores
-   Visualización de los datos de instalación en agregado o por región
-   Comparar el rendimiento de las aplicaciones de escritorio en Windows versiones o en una versión específica, como la versión Windows 10 más reciente o Windows Modo anticipado de Insider y versiones lentas

### <a name="application-blocks-report"></a>Informe de bloques de aplicación

El **informe Bloques** de aplicación le permite ver información sobre Windows 10 dispositivos en los que la aplicación afecta a Windows 10 actualizaciones. Puede ver cuántos dispositivos se ven afectados en un día determinado junto con el número medio de dispositivos en los últimos 30 días.

Los tipos de bloques de actualización incluidos son los siguientes: 

<table>
<tr><th>Category</th><th>Problema</th><th>Descripción</th><th>Instrucciones proporcionadas a los usuarios</th></tr>
<tr><td>Posibles efectos</td><td>Bloqueará la actualización</td><td>La aplicación no funcionará en la nueva versión del sistema operativo. Se requiere una acción del usuario durante la instalación para continuar con la actualización.</td><td>Quite la aplicación antes de actualizar y compruebe con el desarrollador una versión compatible de la aplicación.</td></tr>
<tr><td>Temporal</td><td>Puede bloquear la actualización. Es necesario probar la aplicación.</td><td>Microsoft está investigando los problemas de actualización relacionados con esta aplicación. La actualización no se pondrá en marcha para los usuarios que puedan resultar afectados.</td><td>Quite la aplicación antes de actualizar y compruebe con el desarrollador una versión compatible de la aplicación.</td></tr>
<tr><td>Notificación en tiempo de ejecución</td><td>Puede que no funcione correctamente en la nueva versión del sistema operativo, pero no bloqueará la actualización.</td><td>La aplicación no impedirá la actualización, pero se detectaron problemas que pueden impedir que funcione correctamente en la nueva versión del sistema operativo.</td><td>No es necesario realizar ninguna acción para que la actualización continúe, pero asegúrese de probar la aplicación en la nueva versión del sistema operativo y compruebe con el desarrollador una versión compatible, si es necesario.</td></tr>
</table>

### <a name="retrieve-analytic-data-using-the-microsoft-store-analytics-api"></a>Recuperación de datos analíticos mediante la API Microsoft Store analytics

La API Microsoft Store analytics le permite recuperar mediante programación los datos de análisis de las aplicaciones que ha agregado a su cuenta.

Esta API ofrece los métodos siguientes específicos del programa Windows aplicación de escritorio:

-   [Instala](/windows/uwp/monetize/get-desktop-app-installs)
-   [Aciertos de error](/windows/uwp/monetize/get-desktop-application-error-reporting-data)
-   [Detalles del error](/windows/uwp/monetize/get-details-for-an-error-in-your-desktop-application)
-   [Seguimiento de la pila](/windows/uwp/monetize/get-the-stack-trace-for-an-error-in-your-desktop-application)
-   [Archivo CAB](/windows/uwp/monetize/download-the-cab-file-for-an-error-in-your-desktop-application)
-   [Bloques de actualización](/windows/uwp/monetize/get-desktop-block-data)
-   [Detalles del bloque de actualización](/windows/uwp/monetize/get-desktop-block-data-details)


Para obtener más información sobre el uso de esta API, consulte [Acceso a datos analíticos mediante los servicios de Store.](/windows/uwp/monetize/access-analytics-data-using-windows-store-services)

## <a name="managing-your-desktop-application-metadata"></a>Administración de los metadatos de la aplicación de escritorio

Usamos el nombre de archivo, la versión del archivo, el nombre del producto y los metadatos de la versión del producto en los archivos ejecutables para deducir las agrupaciones lógicas de ejecutables en las aplicaciones. Si los archivos ejecutables no tienen metadatos  precisos, pueden aparecer juntos bajo un nombre de aplicación desconocido o el nombre de la aplicación se establecerá de forma predeterminada en el nombre ejecutable individual.

Mantener actualizados los metadatos de las aplicaciones y los archivos ayuda a garantizar que se representan correctamente en el panel. Estas son algunas recomendaciones:

-   Use el certificado para firmar todos los archivos ejecutables que quiera ver en el informe de análisis, no solo los ejecutables de instalación.
-   Proporcione información coherente sobre el nombre del producto y la versión del producto para todos los archivos ejecutables que pertenecen a la misma aplicación (es decir, *Mi aplicación*). Si algunos de los archivos ejecutables se distribuyen con varias aplicaciones, asíéntesles nombres únicos (es *decir,* componentes compartidos) para que pueda ver el análisis de esos ejecutables por separado de las aplicaciones con las que se distribuyeron.
-   Cada vez que realice cambios en los metadatos, es posible que vea una nueva entrada para la aplicación en el panel. Si realiza un cambio, los nuevos datos de telemetría entrantes reflejarán los cambios, pero los datos de telemetría antiguos seguirán apareciendo como **una aplicación** desconocida.
-   Al revisar un archivo, asegúrese de actualizar los números de versión de la aplicación y del producto.
    > [!Tip]  
    > Use [**los recursos VERSIONINFO**](/windows/desktop/menurc/versioninfo-resource) para establecer **FileDescription,** **FileVersion,** **ProductName** y **ProductVersion** para sus archivos y aplicaciones. En el ejemplo siguiente se define **un recurso VERSIONINFO:**
    >
    > ``` syntax
    > #define VER_PRODUCTNAME_STR      "Sample App"
    > #define VER_PRODUCTVERSION       3,10,349,0
    > #define VER_PRODUCTVERSION_STR   "3.10.349.0\0"
    > #define VER_FILEDESCRIPTION_STR  "Sample File"
    > #define VER_FILEVERSION          3,10,349,0
    > #define VER_FILEVERSION_STR      "3.10.349.0\0"
    > #define VER_COMPANYNAME_STR     "XYZ Corp."
    > #define VER_LEGALCOPYRIGHT_STR   "Copyright \251 XYZ Corp." 
    >  
    > VS_VERSION_INFO VERSIONINFO
    > FILEVERSION VER_FILEVERSION
    > PRODUCTVERSION VER_PRODUCTVERSION
    > FILEFLAGSMASK VER_FILEFLAGSMASK
    > FILEFLAGS VER_FILEFLAGS
    > FILEOS VER_FILEOS
    > FILETYPE VER_FILETYPE
    > FILESUBTYPE VER_FILESUBTYPE
    > BEGIN
    >     BLOCK "StringFileInfo"
    >     BEGIN
    >         BLOCK "040904E4"
    >         BEGIN
    >             VALUE "ProductName",      VER_PRODUCTNAME_STR
    >             VALUE "ProductVersion",   VER_PRODUCTVERSION_STR
    >             VALUE "FileDescription",  VER_FILEDESCRIPTION_STR
    >             VALUE "FileVersion",      VER_FILEVERSION_STR
    >             VALUE "CompanyName",      VER_COMPANYNAME_STR
    >             VALUE "LegalCopyright",   VER_LEGALCOPYRIGHT_STR
    >         END
    >     END
    >      
    > END 
    > ```

     

## <a name="add-and-manage-account-users"></a>Agregar y administrar usuarios de la cuenta

Puede usar Azure Active Directory para agregar y administrar usuarios adicionales en la cuenta Windows programa de aplicaciones de escritorio. Puede agregar usuarios individuales, grupos de usuarios o aplicaciones Azure AD, lo que da a cada uno un rol predefinido (Administrador o Desarrollador).

### <a name="associate-azure-active-directory-with-your-account"></a>Asociación Azure Active Directory con su cuenta

Para agregar y administrar usuarios de cuenta, primero debe asociar la cuenta a la cuenta de la Azure Active Directory. Si la organización ya usa Office 365 u otros servicios empresariales de Microsoft, ya tienes Azure AD. De lo contrario, puede crear un nuevo inquilino Azure AD sin cargo adicional.

Consulte [Associate Azure Active Directory with your Centro de partners account](/windows/uwp/publish/associate-azure-ad-with-dev-center) (Asociar Azure Active Directory con su cuenta de Centro de partners para obtener más información). Aunque el tema se centra en el programa para desarrolladores Windows aplicaciones, la asociación de un inquilino funciona de la misma manera para el Windows aplicación de escritorio.

### <a name="add-users-groups-and-azure-ad-applications-to-your-account"></a>Agregar usuarios, grupos y aplicaciones Azure AD a su cuenta

Una vez que haya configurado la asociación Azure AD, puede agregar usuarios; para ello, vaya a la sección Usuarios en Configuración de la cuenta. A cada usuario se le asigna un rol que define su acceso a la cuenta. También puede agregar grupos de usuarios y aplicaciones Azure AD para concederles acceso a su cuenta Centro de partners usuario. Para obtener más información sobre cómo agregar usuarios, vea [Agregar usuarios, grupos y Azure AD aplicaciones](/windows/uwp/publish/add-users-groups-and-azure-ad-applications).

A cada usuario, grupo o Azure AD aplicación que agregue a su cuenta se le debe asignar un rol. Este proceso se describe en [Establecer roles o permisos personalizados para usuarios de cuenta.](/windows/uwp/publish/set-custom-permissions-for-account-users) Sin embargo, tenga en cuenta que para Windows programa de aplicaciones de escritorio, no hay ninguna capacidad para asignar permisos personalizados o restringir el acceso por producto. En su lugar, a cada usuario se le debe asignar uno de los siguientes roles estándar.



| Rol      | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Manager   | Puede cargar y quitar certificados y puede ver todos los datos analíticos. Tiene acceso completo a la cuenta, excepto para cambiar la información financiera. Esto incluye la administración de usuarios, pero tenga en cuenta que la capacidad de crear y eliminar usuarios en el inquilino de Azure AD depende del permiso de la cuenta en Azure AD. Es decir, si a un usuario se le asigna el rol De administrador, pero no tiene permisos de administrador global en el Azure AD de la organización, no podrá crear nuevos usuarios ni eliminar usuarios del directorio (aunque puede cambiar el rol de cuenta de un usuario).<br/> Tenga en cuenta que si su cuenta está asociada a más de un inquilino de Azure AD, un administrador no puede ver detalles completos de un usuario (incluidos el nombre, los apellidos, el correo electrónico de recuperación de contraseñas y si es un administrador global de Azure AD), a menos que haya iniciado sesión en el mismo inquilino que ese usuario con una cuenta que tenga permisos de administrador global para ese inquilino. Sin embargo, pueden agregar y quitar usuarios en cualquier inquilino asociado a la cuenta. <br/> |
| Desarrollador | Puede ver las aplicaciones y los detalles del certificado asociados a la cuenta, y puede ver el **informe Mantenimiento** **e** instalación. No se puede ver la información financiera ni la configuración de la cuenta.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |



 

## <a name="faq"></a>Preguntas más frecuentes

-   **¿Por qué no veo ningún dato para una aplicación?** No mostraremos datos hasta que detectemos suficientes usuarios para recopilar información significativa. Si acaba de publicar la aplicación, puede tardar algún tiempo en alcanzar este umbral de adopción mínimo. Otro motivo por el que es posible que no vea los datos es si no ha firmado un archivo con el certificado para una aplicación determinada. Asegúrese de cargar los archivos firmados con cada certificado que use para firmar las aplicaciones.
-   **¿Puedo acceder a estos datos a través de una API?** Sí, los datos estarán disponibles a través de una API pública cuando el programa esté disponible para todos los desarrolladores.
-   **¿Qué sucede con las aplicaciones con certificados anteriores?** Desafortunadamente, no se admite el envío de certificados que han expirado o revocado, aunque los renueve con la misma clave.
-   **¿Por qué veo una aplicación que no se reconoce?** Si el certificado que usa para firmar archivos en la aplicación también lo usa otra persona de su empresa para firmar otra aplicación, también verá telemetría para esa aplicación. En el futuro, proporcionaremos una opción para ocultar las aplicaciones del panel. Si su cuenta de empresa está asociada Azure AD un inquilino de Azure AD, puede solicitar al administrador que modifique los permisos de usuario para que solo pueda ver aplicaciones específicas.
-   **¿Cómo puedo proporcionar comentarios sobre la experiencia u obtener soporte técnico?** Si necesita ayuda, puede crear una solicitud de soporte técnico [aquí.](https://developer.microsoft.com/windows/support/) Para compartir sus comentarios, use el vínculo **Comentarios** (en Configuración de la **cuenta)** y seleccione el área **Análisis** para hacernos saber lo que piensa. 
 

