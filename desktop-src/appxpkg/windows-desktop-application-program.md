---
title: Programa de aplicaciones de escritorio de Windows
description: Puede obtener datos de telemetría detallados e informes de análisis que le permitan ver el funcionamiento de las aplicaciones de escritorio de Windows a través del nuevo programa de aplicación de escritorio de Windows.
ms.assetid: F1ED72A5-E1CD-4924-A81B-ED6FAF5E2AA3
ms.topic: article
ms.date: 11/02/2018
ms.openlocfilehash: 2dc255c9c8696bd57198f50fc2c570f59c4ae603
ms.sourcegitcommit: 0bfbb2324081644171495734f0609335173745ef
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/25/2021
ms.locfileid: "105709278"
---
# <a name="windows-desktop-application-program"></a>Programa de aplicaciones de escritorio de Windows

Puede obtener datos de telemetría detallados e informes de análisis que le permitan ver el funcionamiento de las aplicaciones de escritorio de Windows a través del nuevo programa de aplicación de escritorio de Windows.

No es necesario tener acceso a estos datos lo único que tiene que hacer es [registrarse](https://login.microsoftonline.com/common/oauth2/authorize?client_id=4990cffe-04e8-4e8b-808a-1175604b879f&response_mode=form_post&response_type=code+id_token&scope=openid+profile&state=OpenIdConnect.AuthenticationProperties%3deJsPaLaK4fU55nKvN21CjU6FsdJ0aPGfhsjGAZ0HR9bE6rgwHHX4izvRt_w-0VUlIF0ClCya4cVY6Uv4qTAqDrH8LTwFpjFGWVW2BAIJmAAuxBLZGTPS_DYy0wwgvTh1orWTCMvBdlOu_kF8vwNe4mjtk9JRMvYaETyspKrJi-s5Z2K7lKIPqnlFkwSU-aoot-3NxTeQ0wu6_RJ1nf_kLFatEkVAqokDSYTKkpv7zF6gA3YYriMFoC9_f2uxuXpI-STckg&nonce=637177463062493881.YjhiOTZjYTMtOTVhZS00OGM1LWI4MDItNWE5MThjMjA1ZjZmMTAyZDRiMGQtMDJhNC00ZDJmLWFkM2QtM2FjZDJkNjcxYWQy&redirect_uri=https%3a%2f%2fpartner.microsoft.com%2faad%2fauthPostGateway&resource=797f4846-ba00-4fd7-ba43-dac1f8f63013&mkt=en-US) y aceptar el [contrato de programa de aplicación de escritorio de Windows](https://go.microsoft.com/fwlink/?linkid=853677)y, a continuación, cargar un archivo firmado con el mismo certificado que usó para firmar los archivos ejecutables de la aplicación.

## <a name="join-the-windows-desktop-application-program"></a>Unirse al programa de aplicación de escritorio de Windows

**Si su empresa ya tiene una cuenta del centro de Partners**: inicie sesión en su cuenta del centro de Partners (con el cuenta Microsoft asociado al propietario de la cuenta) y vaya a la página **programas** (en **configuración** de la cuenta o seleccionando **todo** en el menú de navegación izquierdo). En **programa de aplicación de escritorio de Windows**, haga clic en **Introducción** para unirse al programa sin costo adicional. Si tiene un inquilino de Azure AD asociado a su cuenta del centro de Partners, los usuarios que haya agregado podrán acceder al programa de aplicación de escritorio de Windows. Próximamente, se le permite establecer un acceso más granular para este programa.

> [!Tip]  
> Si su empresa tiene una cuenta del centro de Partners, pero no tiene acceso a ella, pida al administrador que [le agregue como usuario](/windows/uwp/publish/add-users-groups-and-azure-ad-applications). Tenga en cuenta que solo el propietario de la cuenta puede unirse al programa de aplicación de escritorio de Windows.

 

**Si su empresa no tiene una cuenta del centro de Partners**: puede [registrarse para el programa de aplicación de escritorio de Windows directamente](https://login.microsoftonline.com/common/oauth2/authorize?client_id=4990cffe-04e8-4e8b-808a-1175604b879f&response_mode=form_post&response_type=code+id_token&scope=openid+profile&state=OpenIdConnect.AuthenticationProperties%3dWc5R_wIKVD0EbOy2UUxS0_0GQJnIAbD-eisMn7Gb4cJL18fRdelvbtj5_R0zoGlsebcnAxIvwKS5kx4Ma4mLMbU4l9ULsE9ajiZU4wtchLJXyJGsPCjCBUNV7TY1SzwXAI-LepSoXkqa8xSywVb7JZ3Xed-Lcw-kwEShFOwt0SdSdc1nNevHbPOhotOeFQcqbo0HESVYXk6pZORJ_OYimG99onp_zSTyludOvvaTd9GYKUgX9exCU5IHReP7MzJDHOgqTg&nonce=637177463071243612.NDU4MjE2ZTMtNmVkMi00YWNiLWEzZGEtMjYyNDRkODI0M2FmOTM3MmE1NzgtMzQ1OC00M2ZkLWJhMDktYzI4YTNhNzdiYTk0&redirect_uri=https%3a%2f%2fpartner.microsoft.com%2faad%2fauthPostGateway&resource=797f4846-ba00-4fd7-ba43-dac1f8f63013&mkt=en-US) sin costo alguno. Próximamente, proporcionaremos la opción de [asociar un inquilino de Azure ad con su cuenta](/windows/uwp/publish/add-users-groups-and-azure-ad-applications) para que otras personas de su empresa también puedan iniciar sesión.

## <a name="add-your-desktop-applications"></a>Agregar las aplicaciones de escritorio

Una vez que se ha unido al programa, deberá agregar las aplicaciones de escritorio de Windows al panel para que podamos empezar a mostrar los informes de análisis.

Usamos la firma de código para establecer la identidad de la empresa y recuperar el análisis de las aplicaciones que publique.

Le proporcionaremos un archivo y le pedirá que lo firme con los mismos certificados de firma de código válidos, no expirados que se usan para firmar las aplicaciones de escritorio. Después, cargará ese archivo firmado en el panel. Esto nos permite saber que las aplicaciones de escritorio firmadas con el mismo certificado pertenecen a su cuenta. No usamos la información del certificado para ningún otro propósito.

> [!Important]  
> No es necesario repetir este proceso si lanza una nueva aplicación de escritorio. Una vez que haya cargado el archivo firmado, se identificarán automáticamente las nuevas aplicaciones que estén firmadas con el mismo certificado y se recuperará automáticamente el análisis de esos productos. Tampoco es necesario distribuir el archivo proporcionado dentro de las aplicaciones ni enviar ningún tipo de asignación para los productos.

 

**Para agregar una o más aplicaciones de escritorio**

1.  En el panel, seleccione **agregar aplicaciones de escritorio**.
2.  En la página siguiente, descargue el archivo que se puede firmar seleccionando **descargar el archivo** y, a continuación, guarde el archivo en el equipo.
3.  Firme el archivo que acaba de descargar con el mismo certificado de firma de código que usa para autenticar las aplicaciones de escritorio. Puede usar SignTool.exe (disponible en Microsoft Visual Studio y como parte de la [Windows SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk)) para firmar este archivo. A continuación se describen más detalles sobre este proceso.
4.  Cargue el archivo que acaba de firmar arrastrándolo al campo (o haga clic para examinar los archivos).
5.  Seleccione **submit (enviar** ) para completar el proceso.

![pasos para agregar aplicaciones de escritorio](images/uploadcert.png)

Si usa más de un certificado de firma de código, puede repetir los pasos anteriores para cada uno de los certificados. Puede descargar, firmar y cargar un archivo para cada certificado actual que use para firmar sus aplicaciones. Sin embargo, solo puede usar un certificado por cada archivo descargado.

Después de completar estos pasos, identificaremos qué aplicaciones de escritorio de Windows están firmadas con el mismo certificado que usó para firmar el archivo. En la mayoría de los casos, empezamos a mostrar los informes analíticos en un plazo de 48 horas, aunque a veces puede tardar un poco más.

## <a name="use-signtoolexe-to-sign-the-downloaded-file"></a>Usar signtool.exe para firmar el archivo descargado

Microsoft proporciona una herramienta para firmar archivos, SignTool.exe, con Visual Studio y en el [Windows SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk). Puede utilizar esta herramienta para realizar y comprobar el proceso de firma de código. [Aquí](/dotnet/framework/tools/signtool-exe)encontrará más información sobre SignTool.exe.

A continuación se muestran dos de las formas más comunes de usar esta herramienta para firmar el archivo que se puede firmar.

-   Si tiene acceso al certificado de firma de código como un archivo de [intercambio de información personal (pfx)](/windows-hardware/drivers/install/personal-information-exchange---pfx--files) :

    ``` syntax
    signtool sign /f MyCert.pfx /p MyCertPassword /v SignableFile.bin
    ```

    ![Captura de pantalla que muestra una ventana del símbolo del sistema que muestra el comando ' SignTool Sign/f MyCert. pfx/p MyCertPassword/v SignableFile. bin '.](images/signtool2.png)

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

Una vez cargados los archivos firmados e identificados las aplicaciones de escritorio, el panel mostrará una visión general de las aplicaciones junto con las métricas clave.

Nuestros datos de telemetría mostrarán información de estado como bloqueos para cada aplicación asociada con el certificado. El panel mostrará información general de las aplicaciones junto con las métricas clave. Puede seleccionar cualquier aplicación para ver su informe de [mantenimiento](#health-report), el [Informe de instalaciones](#installs-report)y el informe de [bloques](#application-blocks-report) en el panel. También puede [recuperar datos analíticos mediante programación con la API de análisis de Microsoft Store](#retrieve-analytic-data-using-the-microsoft-store-analytics-api).

> [!Note]  
> Si se detecta que los metadatos de una aplicación se han actualizado para usar un nombre nuevo, se comienza a notificar nuevos datos con el nuevo nombre. Los datos históricos asociados al nombre anterior se conservarán durante 30 días.
> 
> Los análisis no estarán disponibles para una aplicación hasta que se haya instalado en al menos 100 dispositivos.


### <a name="health-report"></a>Informe de estado

El informe de **mantenimiento** le permite obtener datos relacionados con el rendimiento y la calidad de la aplicación, incluidos los bloqueos y los eventos que no responden. Si procede, puede ver los seguimientos de la pila y/o los archivos. CAB para una depuración posterior.

![Informe de mantenimiento: programa de aplicación de escritorio de Windows](images/health.png)

Puede filtrar los datos de varias maneras, lo que le permite:

-   Ver un resumen de todos los tipos de error, ordenados por número de visitas
-   Explorar en profundidad un error determinado y descargar los seguimientos de la pila para depurar el problema más rápido
-   Comparar una nueva versión de la aplicación con las versiones anteriores
-   Ver los datos de estado en agregado o por región, lo que permite aislar los problemas que son específicos de una región.
-   Comparar el rendimiento de las aplicaciones de escritorio en las versiones de Windows o en una versión específica, como la versión más reciente de Windows 10
-   Ver la información de estado de un archivo ejecutable determinado incluido en la aplicación

Seleccione **cargar símbolos** en la parte superior de la tabla **errores** para cargar un archivo. zip que contenga los [archivos de símbolos](http:/docs.microsoft.com/windows-hardware/drivers/debugger/symbols-and-symbol-files)de la aplicación. Estos archivos de símbolos se indexarán y se usarán para generar seguimientos de pila más precisos. Los tipos de archivos de símbolos del archivo. zip deben ser. pdb,. dll o. exe. Después de cargar correctamente el archivo. zip, debería ver menos **. Valores desconocidos** para los nuevos errores en la lista de errores de la aplicación en aproximadamente 5 días.

### <a name="installs-report"></a>Instala el informe

El informe de **instalaciones** le permite ver el número de dispositivos en los que se instaló una aplicación para un día determinado y el promedio de dispositivos en los que se instaló cada versión de la aplicación en los últimos 30 días.

Puede filtrar los datos de varias maneras, lo que le permite:

-   Ver un resumen de las instalaciones, ordenadas por popularidad
-   Comparar una nueva versión de la aplicación con las versiones anteriores
-   Ver los datos de instalación en agregado o por región
-   Compare el rendimiento de las aplicaciones de escritorio en todas las versiones de Windows o en una versión específica, como la versión más reciente de Windows 10 o las versiones más lentas y lentas de Windows Insider

### <a name="application-blocks-report"></a>Informe de bloques de aplicación

El informe de **bloques de aplicación** le permite ver información sobre los dispositivos de Windows 10 en los que la aplicación afecta a las actualizaciones de Windows 10. Puede ver cuántos dispositivos se ven afectados en un día determinado junto con el promedio de dispositivos durante los últimos 30 días.

Los tipos de bloques de actualización incluidos son los siguientes: 

<table>
<tr><th>Category</th><th>Problema</th><th>Descripción</th><th>Instrucciones proporcionadas a los usuarios</th></tr>
<tr><td>Sedimentos potenciales</td><td>Bloqueará la actualización</td><td>La aplicación no funcionará en la nueva versión de lanzamiento del sistema operativo. La acción del usuario es necesaria durante la instalación para continuar con la actualización.</td><td>Quite la aplicación antes de actualizar y consulte con el desarrollador una versión compatible de la aplicación.</td></tr>
<tr><td>Sedimentos temporales</td><td>Puede bloquear la actualización. Necesidad de probar la aplicación.</td><td>Microsoft está investigando los problemas de actualización relacionados con esta aplicación. La actualización no se implementará para los usuarios que puedan verse afectados.</td><td>Quite la aplicación antes de actualizar y consulte con el desarrollador una versión compatible de la aplicación.</td></tr>
<tr><td>Notificación en tiempo de ejecución</td><td>Puede que no funcione correctamente en la nueva versión de lanzamiento del sistema operativo, pero no bloqueará la actualización</td><td>La aplicación no impedirá la actualización, pero se detectaron problemas que pueden impedir que funcione correctamente en la nueva versión de lanzamiento del sistema operativo.</td><td>No es necesario realizar ninguna acción para que la actualización continúe, pero asegúrese de probar la aplicación en la nueva versión de lanzamiento del sistema operativo y, si es necesario, consulte con el desarrollador una versión compatible.</td></tr>
</table>

### <a name="retrieve-analytic-data-using-the-microsoft-store-analytics-api"></a>Recuperación de datos analíticos mediante la API de análisis de Microsoft Store

La API de Microsoft Store Analytics le permite recuperar mediante programación los datos de análisis de las aplicaciones que ha agregado a su cuenta.

Esta API ofrece los siguientes métodos específicos del programa de aplicación de escritorio de Windows:

-   [Instala](/windows/uwp/monetize/get-desktop-app-installs)
-   [Aciertos de errores](/windows/uwp/monetize/get-desktop-application-error-reporting-data)
-   [Detalles del error](/windows/uwp/monetize/get-details-for-an-error-in-your-desktop-application)
-   [Seguimiento de la pila](/windows/uwp/monetize/get-the-stack-trace-for-an-error-in-your-desktop-application)
-   [Archivo. CAB](/windows/uwp/monetize/download-the-cab-file-for-an-error-in-your-desktop-application)
-   [Bloques de actualización](/windows/uwp/monetize/get-desktop-block-data)
-   [Detalles del bloque de actualización](/windows/uwp/monetize/get-desktop-block-data-details)


Para obtener más información sobre el uso de esta API, consulte [acceso a datos analíticos con servicios](/windows/uwp/monetize/access-analytics-data-using-windows-store-services)de la tienda.

## <a name="managing-your-desktop-application-metadata"></a>Administrar los metadatos de la aplicación de escritorio

Usamos el nombre de archivo, la versión del archivo, el nombre del producto y los metadatos de la versión del producto en los archivos ejecutables para deducir las agrupaciones lógicas de los ejecutables en las aplicaciones. Si los archivos ejecutables no tienen metadatos precisos, pueden aparecer juntos en un nombre de aplicación **desconocido** , o el nombre de la aplicación se establecerá de forma predeterminada en el nombre del archivo ejecutable individual.

Mantener actualizados los metadatos de las aplicaciones y los archivos ayuda a asegurarse de que se representan correctamente en el panel. Estas son algunas recomendaciones:

-   Use el certificado para firmar todos los archivos ejecutables que desee ver en el informe de análisis, no solo los ejecutables del programa de instalación.
-   Proporcione el nombre de producto y la información de versión de producto coherentes para todos los archivos ejecutables que pertenezcan a la misma aplicación (es decir, *mi aplicación*). Si algunos de los archivos ejecutables se distribuyen con varias aplicaciones, asígneles nombres únicos (es decir, *componentes compartidos*) para que pueda ver el análisis de esos ejecutables de forma independiente de las aplicaciones con las que se distribuyeron.
-   Cada vez que realice cambios en los metadatos, puede ver una nueva entrada para la aplicación en el panel. Si realiza un cambio, los nuevos datos de telemetría entrantes reflejarán los cambios, pero los datos de telemetría antiguos seguirán apareciendo como una aplicación **desconocida** .
-   Al revisar un archivo, asegúrese de actualizar la versión de la aplicación y los números de versión del producto.
    > [!Tip]  
    > Use los recursos [**versionInfo**](/windows/desktop/menurc/versioninfo-resource) para establecer **FileDescription**, **fileversion**, **ProductName** y **ProductVersion** para sus archivos y aplicaciones. En el ejemplo siguiente se define un recurso **versionInfo** :
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

Puede usar Azure Active Directory para agregar y administrar usuarios adicionales en la cuenta de programa de aplicación de escritorio de Windows. Puede Agregar usuarios individuales, grupos de usuarios o Azure AD aplicaciones, y asignar a cada uno un rol predefinido (administrador o desarrollador).

### <a name="associate-azure-active-directory-with-your-account"></a>Asociar Azure Active Directory con su cuenta

Para agregar y administrar usuarios de cuenta, primero debe asociar la cuenta con el Azure Active Directory de su organización. Si la organización ya usa Office 365 u otros servicios empresariales de Microsoft, ya tienes Azure AD. De lo contrario, puede crear un nuevo inquilino de Azure AD sin cargo adicional.

Para obtener más información, consulte [asociar Azure Active Directory con su cuenta del centro de Partners](/windows/uwp/publish/associate-azure-ad-with-dev-center) . Aunque el tema se centra en el programa para desarrolladores de aplicaciones de Windows, la Asociación de un inquilino funciona de la misma manera para el programa de aplicación de escritorio de Windows.

### <a name="add-users-groups-and-azure-ad-applications-to-your-account"></a>Agregar usuarios, grupos y aplicaciones Azure AD a su cuenta

Una vez que haya configurado la Asociación de Azure AD, puede Agregar usuarios en la sección usuarios, en configuración de la cuenta. A cada usuario se le asigna un rol que define su acceso a la cuenta. También puede agregar grupos de usuarios y Azure AD aplicaciones para concederles acceso a su cuenta del centro de Partners. Para obtener más información sobre cómo agregar usuarios, vea [Agregar usuarios, grupos y aplicaciones Azure ad](/windows/uwp/publish/add-users-groups-and-azure-ad-applications).

A cada usuario, grupo o aplicación Azure AD que agregue a su cuenta se le debe asignar un rol. Este proceso se describe en [establecer roles o permisos personalizados para usuarios de la cuenta](/windows/uwp/publish/set-custom-permissions-for-account-users). Sin embargo, tenga en cuenta que para el programa de aplicación de escritorio de Windows, no existe la posibilidad de asignar permisos personalizados o restringir el acceso por producto. En su lugar, cada usuario debe tener uno de los siguientes roles estándar.



| Role      | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Manager   | Puede cargar y quitar certificados y puede ver todos los datos analíticos. Tiene acceso completo a la cuenta, excepto para cambiar la información financiera. Esto incluye la administración de usuarios, pero tenga en cuenta que la capacidad de crear y eliminar usuarios en el inquilino de Azure AD depende del permiso de la cuenta en Azure AD. Es decir, si a un usuario se le asigna el rol de administrador, pero no tiene permisos de administrador global en el Azure AD de la organización, no podrá crear nuevos usuarios ni eliminar usuarios del directorio (aunque pueden cambiar el rol de cuenta de un usuario).<br/> Tenga en cuenta que si la cuenta está asociada a más de un inquilino de Azure AD, un administrador no podrá ver los detalles completos de un usuario (incluido el nombre, el apellido, el correo electrónico de recuperación de contraseña y si es un administrador global Azure AD) a menos que haya iniciado sesión en el mismo inquilino que ese usuario con una cuenta que tenga permisos de administrador global para ese inquilino. Sin embargo, pueden agregar y quitar usuarios de cualquier inquilino asociado a la cuenta. <br/> |
| Desarrollador | Puede ver las aplicaciones y los detalles del certificado asociados con la cuenta, y puede ver el informe **Estado** e **instalaciones** . No se puede ver la información financiera o la configuración de la cuenta.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |



 

## <a name="faq"></a>Preguntas más frecuentes

-   **¿Por qué no veo ningún dato para una aplicación?** No se mostrarán datos hasta que se detecten suficientes usuarios para recopilar información significativa. Si acaba de lanzar la aplicación, puede tardar algún tiempo en alcanzar este umbral mínimo de adopción. Otro motivo por el que podría no ver los datos es si no ha firmado un archivo con el certificado para una aplicación determinada. Asegúrese de cargar los archivos firmados con todos los certificados que utilice para firmar sus aplicaciones.
-   **¿Puedo tener acceso a estos datos a través de una API?** Sí, los datos estarán disponibles a través de una API pública cuando el programa esté disponible para todos los desarrolladores.
-   **¿Qué ocurre con las aplicaciones con certificados antiguos?** Desafortunadamente, no se admite el envío de certificados que hayan expirado o se hayan revocado, aunque los renueve con la misma clave.
-   **¿Por qué veo una aplicación que no reconozco?** Si el certificado que usa para firmar archivos en la aplicación también lo usa otra persona de su empresa para firmar otra aplicación, también verá la telemetría de esa aplicación. En el futuro, proporcionaremos una opción para ocultar las aplicaciones desde el panel. Si la cuenta de la empresa está asociada a un inquilino de Azure AD, puede solicitar al administrador que modifique los permisos de usuario para que solo puedan ver determinadas aplicaciones.
-   **¿Cómo puedo proporcionar comentarios sobre la experiencia o obtener soporte técnico?** Si necesita ayuda, puede crear una solicitud de soporte técnico [aquí](https://developer.microsoft.com/windows/support/). Para compartir sus comentarios, use el vínculo de **comentarios** (en configuración de la **cuenta**) y seleccione el área de **análisis** para hacernos saber lo que piensa. 
 

