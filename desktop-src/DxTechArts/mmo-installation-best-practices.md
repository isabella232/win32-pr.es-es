---
title: Procedimientos recomendados de instalación para juegos en línea multijugador masivos
description: En este artículo se describe la creación de una cadena de diseño de confianza para la instalación de cliente de Juegos en línea multijugador masivos (MWINDOW) y sistemas de actualización de juegos personalizados que funcionan bien con Windows y el modelo de seguridad de Windows Vista y Windows 7.
ms.assetid: b719cff7-97e8-5e0a-9c91-3bd8178da7c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b574bdf2ae98b28fabed97340d6aa38b1a864c24519bb6532d0aa4069882efe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117815445"
---
# <a name="installation-best-practices-for-massively-multiplayer-online-games"></a>Procedimientos recomendados de instalación para juegos en línea multijugador masivos

En este artículo se describe la creación de una cadena de diseño de confianza para la instalación de cliente de Juegos en línea multijugador masivos (MWINDOW) y sistemas de actualización de juegos personalizados que funcionan bien con Windows y el modelo de seguridad de Windows Vista y Windows 7. El enfoque está diseñado para habilitar la aplicación de revisiones de los títulos de M LDAP a la vez que se admiten cuentas de usuario estándar, que tienen acceso restringido al disco duro y al registro del sistema.

-   [Por qué los clientes M RETAIL tienen distintos requisitos para los juegos tradicionales comprados por el comercio minorista](#why-mmog-clients-have-different-requirements-to-traditional-retail-purchased-games)
-   [Introducción a un enfoque de cadena de confianza](#overview-of-a-chain-of-trust-approach)
-   [Todo se valida en el servidor, ¿por qué debo preocuparme si se piratea mi cliente?](#everything-is-validated-on-the-server-why-should-i-worry-if-my-client-gets-hacked)
-   [Construcción de la aplicación Trust-Worthy Loader](#construction-of-the-trust-worthy-loader-application)
    -   [Lectura en segundo plano](#background-reading)
    -   [Instalación del cargador de confianza y el patcher](#installation-of-the-trusted-loader-and-patcher)
    -   [Instalación de los archivos ejecutables, archivos DLL y datos del juego](#installation-of-the-game-executables-dlls-and-data)
    -   [Access Control de modificación de la lista de cambios](#access-control-list-modification-code)
    -   [Instalaciones para usuarios avanzados](#installations-for-advanced-users)
    -   [Comprobación de confianza del cargador](#the-loaders-verification-of-trust)
    -   [Validación de datos](#data-validation)

## <a name="why-mmog-clients-have-different-requirements-to-traditional-retail-purchased-games"></a>Por qué los clientes M RETAIL tienen distintos requisitos para los juegos tradicionales comprados por el comercio minorista

La naturaleza en constante conexión y evolución de los MMOG hace que sea un requisito fundamental proporcionar actualizaciones periódicas del código de cliente y el contenido para corregir vulnerabilidades de seguridad y ampliar la experiencia de juego. Con la posibilidad de realizar actualizaciones casi diarias, el escenario M MANAGEMENT requiere una administración cuidadosa para garantizar una experiencia fácil de usar. Esto difiere del modelo de compra comercial tradicional, donde se puede proporcionar un pequeño número de revisiones cerca de la fecha de envío comercial del producto. La tecnología de aplicación de revisiones de usuario limitada de Windows Installer proporcionada con el sistema operativo está diseñada para controlar un pequeño número de revisiones de aplicación, y no la gran cantidad y alta frecuencia que necesitan los MMOG. Por lo tanto, a menudo es necesario desarrollar sistemas de revisión personalizados para satisfacer las necesidades de los MMOG, incluidos los requisitos especiales específicos del MOP concreto que se está desarrollando.

Dado que muchos equipos están conectados a Internet, Windows Vista y Windows 7 tienen restricciones de seguridad y medidas de seguridad más difíciles para los usuarios, que limitan el acceso que las aplicaciones tienen a varias áreas del disco duro. A Windows XP, estas restricciones están habilitadas para el modo predeterminado para las cuentas de usuario. Estas restricciones deben tenerse en cuenta al diseñar el diseño de un juego, un archivo ejecutable y los datos, y su sistema de aplicación de revisiones asociado. Para obtener más información sobre las medidas de seguridad proporcionadas por el sistema operativo, vea Control de [cuentas de usuario para desarrolladores de juegos.](/windows/desktop/DxTechArts/user-account-control-for-game-developers)

## <a name="overview-of-a-chain-of-trust-approach"></a>Introducción a un enfoque de cadena de confianza

El enfoque de actualización personalizado que se presenta en estas instrucciones se basa en tener una aplicación de cargador de confianza instalada en la carpeta archivos de programa protegida y, al mismo tiempo, mantener los archivos ejecutables y los datos de los juegos en un área compartida accesible para todo el usuario. Una cadena de confianza comienza con el cargador que realiza comprobaciones de validez en los archivos binarios y los datos del juego antes del lanzamiento.

![La cadena de confianza comienza con un cargador de confianza](images/mmo-installation-best-practices-01.gif)

El cargador de confianza debe tener suficiente lógica para poder comprobar que el archivo ejecutable del juego y otros archivos binarios no se han alterado antes de iniciar el juego. El cargador también puede comprobar los datos del juego tantas veces como sea necesario; sin embargo, el tamaño de los datos del juego suele ser demasiado grande para permitir que se comprueben cada vez en un solo pase. Un enfoque alternativo es usar un patrón de muestreo que garantice que la comprobación de todo el conjunto de datos se produzca durante un largo período de tiempo. La aplicación del cargador puede contener un motor de revisión de juegos, que proporciona un método de confianza para integrar las actualizaciones con el juego instalado.

## <a name="everything-is-validated-on-the-server-why-should-i-worry-if-my-client-gets-hacked"></a>Todo se valida en el servidor, ¿por qué debo preocuparme si se piratea mi cliente?

Es imposible confiar en que el cliente no se ha puesto en peligro; por lo tanto, es habitual que los servidores M RADIUS validen todos los datos recibidos del cliente. Aunque este procesamiento puede identificar clientes de juegos en peligro o en peligro dentro del universo del juego, el servidor no puede identificar fácilmente todos los problemas a los que se puede exponer el cliente del juego. Es importante reforzar la protección contra los hackers que desean usar el cliente como plataforma para ataques a su servicio, a otros usuarios o incluso simplemente como vector para atacar a las propias máquinas cliente. La aplicación de técnicas de firma de código y comprobación de datos puede ayudar a detectar clientes en peligro antes de que se ejecuten. Dado que el mecanismo de aplicación de revisiones requiere exponer archivos binarios ejecutables y DLL que no están protegidos por los permisos estándar de solo lectura en archivos de programa, la validación de estos archivos antes de iniciarlos es importante para la seguridad general del sistema.

Este modelo no intenta tratar con el escenario de usuario administrador malintencionado en el que el propio cargador podría estar en peligro, pero se centra en proteger a los usuarios estándar frente a la ejecución accidental de código alterado. Las técnicas tradicionales de validación de cliente y servidor son realmente la única mitigación posible para los administradores del sistema cliente malintencionados.

## <a name="construction-of-the-trust-worthy-loader-application"></a>Construcción de la aplicación Trust-Worthy Loader

### <a name="background-reading"></a>Lectura en segundo plano

Los lectores deben familiarizarse con la siguiente documentación, que proporciona detalles de la tecnología fundamental para garantizar el procedimiento recomendado para la confianza basada en software.

<dl> <dt>

<span id="Code_Signing"></span><span id="code_signing"></span><span id="CODE_SIGNING"></span>Firma de código
</dt> <dd>

[Firma de Authenticode para desarrolladores de juegos](/windows/desktop/DxTechArts/authenticode-signing-for-game-developers)

</dd> <dt>

<span id="SignTool"></span><span id="signtool"></span><span id="SIGNTOOL"></span>SignTool
</dt> <dd>

[SignTool](/windows/desktop/SecCrypto/signtool) en MSDN

</dd> </dl>

En la sección siguiente se detallan las API que se deben usar para construir la aplicación del cargador, que admiten el diseño de discos para la instalación y comprobación de la comprobación de confianza.

### <a name="installation-of-the-trusted-loader-and-patcher"></a>Instalación del cargador de confianza y el patcher

El cargador de confianza y la versión base de la utilidad patcher deben instalarse en la carpeta Archivos de programa protegida del HDD, igual que en las instalaciones tradicionales. La instalación y aplicación de revisiones de la aplicación de cargador requiere derechos de administrador, por lo que es importante minimizar la frecuencia de actualización del cargador para asegurarse de que los usuarios finales no necesitan elevarse con frecuencia, aunque se podría usar la aplicación de revisiones de usuario limitada de Windows Installer para evitar la elevación de las revisiones del cargador.

Consulte el artículo Patching Game Software en Windows XP, Windows Vista y Windows 7.

### <a name="installation-of-the-game-executables-dlls-and-data"></a>Instalación de los archivos ejecutables, archivos DLL y datos del juego

Para facilitar las actualizaciones de usuario estándar del juego sin privilegios administrativos, el archivo ejecutable, los archivos DLL y los datos de los juegos deben instalarse en un área del disco duro que sea accesible para todos los usuarios. El sistema operativo proporciona un área "Datos de aplicación de todos los usuarios" que se puede usar como ubicación predeterminada para la instalación. [**SHGetFolderPath debe**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) usarse con la clave COMMON APPDATA de CSIDL para determinar la ruta de \_ acceso del archivo para esta \_ área. Es importante no realizar suposiciones sobre la ruta de acceso a la que esta clave devuelve, ya que puede ser configurable por el usuario.

La instalación debe modificar o administrar los permisos de carpeta para lograr el acceso de escritura compartido de todo el usuario necesario para actualizar el título. Con los permisos correctos, la funcionalidad del actualizador de juegos del programa cargador puede aplicar fácilmente revisiones al juego sin necesidad de privilegios especiales de ninguna cuenta de usuario, incluidas las horas en las que los usuarios estándar inician el juego.

### <a name="access-control-list-modification-code"></a>Access Control de modificación de la lista de cambios

Para Windows XP, deberá ejecutar código para cambiar manualmente la lista de control de acceso (ACL), esta es una función de ejemplo que muestra cómo hacerlo:

``` syntax
HRESULT ChangeACLtoAllowUserRW( WCHAR* strDir )
{
    EXPLICIT_ACCESS explicitaccess;
    PACL NewAcl = NULL;
    DWORD dwError;

    BuildExplicitAccessWithName( &explicitaccess, L"BUILTIN\\Users",
                                 GENERIC_ALL, GRANT_ACCESS,
                                 SUB_CONTAINERS_AND_OBJECTS_INHERIT );
                                 
    dwError = SetEntriesInAcl( 1, &explicitaccess, NULL, &NewAcl );
    if( dwError == ERROR_SUCCESS) 
    {
        dwError = SetNamedSecurityInfo( strDir, SE_FILE_OBJECT,
                                        DACL_SECURITY_INFORMATION,
                                        NULL, NULL, NewAcl, NULL );
        if( dwError == ERROR_SUCCESS)
        {
            if( NewAcl != NULL ) AccFree( NewAcl );
            return S_OK;
        }
    }

    if( NewAcl != NULL ) AccFree( NewAcl );
    return E_FAIL;
}
```

Este ejemplo de código también funcionará para Windows Vista y Windows 7; Sin embargo, también proporcionan la utilidad de línea de comandos icacls para editar acls de archivo que puede usar en su lugar.

Sin embargo, la herramienta proporciona una ayuda detallada cuando se ejecuta; sin embargo, un ejemplo de uso de la herramienta es:

``` syntax
icacls "C:\Users\All Users\Game" /grant Rex:(D,WDAC)
```

Este uso concederá al usuario permisos delete y write DAC para la carpeta game almacenada en las áreas Todos los usuarios del disco duro.

### <a name="installations-for-advanced-users"></a>Instalaciones para usuarios avanzados

Para escenarios de instalación de usuarios avanzados, es posible que un usuario quiera especificar manualmente la ruta de instalación de juegos. La selección de directorio debe restringirse a uno fuera de los archivos de programa para asegurarse de que la carpeta se encuentra en un área realmente compartible del disco duro. La ruta de acceso seleccionada por el usuario solo debe usarse para los datos y los exes de juegos, ya que los archivos de juego Loader y Patcher siempre deben instalarse en la carpeta archivos de programa seguros para mejorar la seguridad.

### <a name="the-loaders-verification-of-trust"></a>Comprobación de confianza del cargador

Windows proporciona la [**función WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust) para comprobar la validez del código firmado y se basa en los servicios criptográficos del sistema operativo. La función está totalmente documentada en MSDN: **WinVerifyTrust** Function.

En el programa de ejemplo siguiente de MSDN se detalla el uso de la función para determinar si un ejecutable del programa está firmado con un certificado válido: Programa C de [ejemplo:](/windows/desktop/SecCrypto/example-c-program--verifying-the-signature-of-a-pe-file)Comprobar la firma de un archivo PE .

Para comprobar que el ejecutable de juego firmado es de confianza para ejecutarse desde el cargador, la acción Comprobación genérica será suficiente:

<dl> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor
</dt> <dd>

COMPROBACIÓN GENÉRICA DE LA ACCIÓN DE WINTRUST \_ \_ \_ \_ V2

</dd> <dt>

<span id="Meaning"></span><span id="meaning"></span><span id="MEANING"></span>Significado
</dt> <dd>

Compruebe un archivo u objeto mediante el proveedor de directivas Authenticode.

</dd> </dl>

La función toma un argumento de estructura de entrada que contiene información que el proveedor de confianza necesita para procesar la acción especificada. Normalmente, como en el caso del ejemplo anterior, la estructura incluye información que identifica el objeto que el proveedor de confianza debe evaluar.

El formato de la estructura es específico del identificador de acción. En el tema siguiente de MSDN se detalla la estructura de ejemplo para el proveedor WinTrust: [**ESTRUCTURA DE \_ DATOS WINTRUST.**](/windows/desktop/api/wintrust/ns-wintrust-wintrust_data)

Si el proveedor de confianza comprueba que el sujeto es de confianza para la acción especificada, el valor devuelto es cero. Ningún otro valor además de cero debe considerarse una devolución correcta.

### <a name="data-validation"></a>Validación de datos

El mecanismo de firma de código solo admite la firma de algunos tipos específicos de archivos, incluidos archivos ejecutables, archivos DLL, paquetes del instalador de Windows (archivos .msi) y archivos de archivo (.cab). [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust) API no debe usarse para comprobar que los archivos de datos grandes (por ejemplo, los archivos .cab) no se han alterado, ya que hay algunos problemas de rendimiento y estabilidad al validar archivos muy grandes. Los ejecutables del programa tienden a ser lo suficientemente pequeños como para que se produzca una comprobación de plena confianza mediante el proveedor WinTrust, pero los archivos de datos de los juegos suelen ser del dominio de muchos gigabytes de tamaño. El enfoque que toma el cargador para la comprobación de los datos del juego debe ser uno en el que se prueba una pequeña muestra del conjunto de datos durante el tiempo de ejecución del juego. Este enfoque distribuye el costo de las pruebas de verificación a lo largo de la vida de la experiencia de juego y puede proporcionar una experiencia de usuario sin problemas sin tiempos de espera largos. Para ello, puede ser necesaria una organización cuidadosa de los datos. Algunos MMOG emplean un enfoque de base de datos para ayudar a administrar, mantener y comprobar la corrección de los recursos del juego a lo largo del tiempo.

Desde el punto de vista de la seguridad, el código de cliente debe diseñarse para no confiar en los archivos de datos, incluso si se usa algún tipo de validación de datos básica con el cargador de confianza. Se deben emplear comprobaciones de encabezado, hashes y otras comprobaciones de integridad tradicionales. El trabajo para mejorar el código de E/S del cliente también debe realizarse mediante técnicas como pruebas aproximadas, así como aprovechar las herramientas automáticas de análisis de código estático, como el modificador **/analyze** en Visual Studio 2005 y Visual Studio 2008 (disponible en Visual Studio Team System y el compilador gratuito que se incluye con el SDK de Windows).

Para obtener más información sobre la seguridad de software, vea [Best Security Practices in Game Development](/windows/desktop/DxTechArts/best-security-practices-in-game-development).

 

 