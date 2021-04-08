---
title: Prácticas recomendadas de instalación para juegos en línea multijugador masivo
description: En este artículo se describe cómo crear una cadena de diseño de confianza para la instalación de cliente de juegos de varios jugadores en línea (MMOG) y los sistemas de actualización de juegos personalizados que funcionan bien con Windows y el modelo de seguridad de Windows Vista y Windows 7.
ms.assetid: b719cff7-97e8-5e0a-9c91-3bd8178da7c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e81003a434b830f046c29d606355104fe618d1f5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077986"
---
# <a name="installation-best-practices-for-massively-multiplayer-online-games"></a>Prácticas recomendadas de instalación para juegos en línea multijugador masivo

En este artículo se describe cómo crear una cadena de diseño de confianza para la instalación de cliente de juegos de varios jugadores en línea (MMOG) y los sistemas de actualización de juegos personalizados que funcionan bien con Windows y el modelo de seguridad de Windows Vista y Windows 7. El enfoque está diseñado para habilitar la revisión de los títulos de MMOG al admitir las cuentas de usuario estándar, que tienen acceso restringido a la unidad de disco duro y al registro del sistema.

-   [¿Por qué los clientes de MMOG tienen requisitos diferentes para los juegos de compra minorista tradicionales?](#why-mmog-clients-have-different-requirements-to-traditional-retail-purchased-games)
-   [Información general de un enfoque de cadena de confianza](#overview-of-a-chain-of-trust-approach)
-   [¿Por qué se valida todo en el servidor, ¿por qué debería preocuparse si el cliente se vuelve a atacar?](#everything-is-validated-on-the-server-why-should-i-worry-if-my-client-gets-hacked)
-   [Construcción de la aplicación de cargador de Trust-Worthy](#construction-of-the-trust-worthy-loader-application)
    -   [Lectura en segundo plano](#background-reading)
    -   [Instalación del cargador y el aplicador de confianza](#installation-of-the-trusted-loader-and-patcher)
    -   [Instalación de los archivos ejecutables del juego, los archivos dll y los datos](#installation-of-the-game-executables-dlls-and-data)
    -   [Código de modificación de lista de Access Control](#access-control-list-modification-code)
    -   [Instalaciones para usuarios avanzados](#installations-for-advanced-users)
    -   [Comprobación del cargador de confianza](#the-loaders-verification-of-trust)
    -   [Validación de datos](#data-validation)

## <a name="why-mmog-clients-have-different-requirements-to-traditional-retail-purchased-games"></a>¿Por qué los clientes de MMOG tienen requisitos diferentes para los juegos de compra minorista tradicionales?

La naturaleza constantemente conectada y en constante evolución de MMOGs hace que sea un requisito fundamental proporcionar actualizaciones periódicas del código de cliente y el contenido para corregir las vulnerabilidades de seguridad y ampliar la experiencia de juego. Con la posibilidad de que se produzcan actualizaciones casi diarias, el escenario MMOG requiere una administración cuidadosa para garantizar una experiencia de usuario sencilla. Esto difiere del modelo de compra minorista tradicional en el que se puede proporcionar un pequeño número de revisiones cerca de la fecha de envío comercial del producto. El Windows Installer tecnología de aplicación de revisiones de usuarios limitada que se proporciona con el sistema operativo se ha diseñado para controlar un número reducido de revisiones de la aplicación, y no la gran cantidad y la frecuencia alta que necesita MMOGs. Por lo tanto, a menudo es necesario que los sistemas de revisión personalizados se desarrollen para satisfacer las necesidades de MMOGs, incluidos los requisitos especiales específicos de la MMOG en particular que se está desarrollando.

Dado que hay muchos equipos conectados a Internet, Windows Vista y Windows 7 tienen restricciones de seguridad y medidas de seguridad más estrictas para los usuarios, lo que limita el acceso que tienen las aplicaciones a diversas áreas del disco duro. A diferencia de Windows XP, estas restricciones están habilitadas para el modo predeterminado para las cuentas de usuario. Estas restricciones se deben tener en cuenta al diseñar el diseño de un juego, un ejecutable y datos, y su sistema de aplicación de revisiones asociado. Para obtener más información sobre las medidas de seguridad proporcionadas por el sistema operativo, consulte [control de cuentas de usuario para desarrolladores de juegos](/windows/desktop/DxTechArts/user-account-control-for-game-developers).

## <a name="overview-of-a-chain-of-trust-approach"></a>Información general de un enfoque de cadena de confianza

El enfoque de actualización personalizada que se presenta en esta nota del producto se basa en la instalación de una aplicación de cargador confiable en la carpeta archivos de programa protegidos, a la vez que mantiene los archivos ejecutables y los datos de los juegos en un área accesible para todo el usuario. Una cadena de confianza comienza con el cargador que realiza comprobaciones de validez en los archivos binarios y datos del juego antes del inicio.

![la cadena de confianza comienza con un cargador de confianza](images/mmo-installation-best-practices-01.gif)

El cargador de confianza debe tener suficiente lógica para poder comprobar que el ejecutable del juego y otros archivos binarios no se han manipulado antes de iniciar el juego. El cargador también puede comprobar los datos del juego tantas veces como sea necesario. sin embargo, el tamaño de los datos del juego suele ser demasiado grande para permitir que se compruebe cada vez en un solo paso. Un enfoque alternativo es usar un patrón de muestreo que garantice que la comprobación del conjunto de datos completo se produce durante un período de tiempo prolongado. La aplicación de cargador puede contener un motor de revisión de juegos, que proporciona un método digno de confianza por para integrar las actualizaciones con el juego instalado.

## <a name="everything-is-validated-on-the-server-why-should-i-worry-if-my-client-gets-hacked"></a>¿Por qué se valida todo en el servidor, ¿por qué debería preocuparse si el cliente se vuelve a atacar?

No es posible confiar en que el cliente no se ha puesto en peligro; por lo tanto, es común que los servidores de MMOG validen todos los datos recibidos del cliente. Aunque este procesamiento puede identificar a los clientes de juegos en peligro o a través del universo del juego, el servidor no puede identificar fácilmente todos los problemas a los que se puede exponer el cliente del juego. Es importante reforzar la protección frente a los hackers que desean usar su cliente como plataforma para los ataques en el servicio, otros usuarios o incluso un vector para atacar los propios equipos cliente. La aplicación de técnicas de firma de código y comprobación de datos puede ayudar a detectar los clientes en peligro antes de que se ejecuten. Puesto que el mecanismo de aplicación de revisiones requiere exponer archivos ejecutables y binarios de DLL que no están protegidos por los permisos de solo lectura estándar en los archivos de programa, la validación de estos archivos antes de iniciarlos es importante para la seguridad global del sistema.

Este modelo no intenta tratar con el escenario de usuario de administrador malintencionado en el que el propio cargador podría quedar en peligro, sino que se centra en la protección de los usuarios estándar para que ejecuten código alterado accidentalmente. Las técnicas tradicionales de validación de cliente de servidor son, en realidad, la única mitigación posible para los administradores de sistemas cliente malintencionados.

## <a name="construction-of-the-trust-worthy-loader-application"></a>Construcción de la aplicación de cargador de Trust-Worthy

### <a name="background-reading"></a>Lectura en segundo plano

Los lectores deben familiarizarse con la siguiente documentación, que proporciona detalles de la tecnología de base para garantizar las prácticas recomendadas para la confianza basada en software.

<dl> <dt>

<span id="Code_Signing"></span><span id="code_signing"></span><span id="CODE_SIGNING"></span>Firma de código
</dt> <dd>

[Firma de Authenticode para desarrolladores de juegos](/windows/desktop/DxTechArts/authenticode-signing-for-game-developers)

</dd> <dt>

<span id="SignTool"></span><span id="signtool"></span><span id="SIGNTOOL"></span>SignTool
</dt> <dd>

[SignTool](/windows/desktop/SecCrypto/signtool) en MSDN

</dd> </dl>

En la siguiente sección se detallan las API que se deben usar para construir la aplicación del cargador, que admiten el diseño del disco para la instalación y comprobación de la comprobación de confianza.

### <a name="installation-of-the-trusted-loader-and-patcher"></a>Instalación del cargador y el aplicador de confianza

El cargador de confianza y la versión base de la utilidad de revisión deben instalarse en la carpeta archivos de programa protegidos en la unidad de disco duro, al igual que en las instalaciones tradicionales. La instalación y aplicación de revisiones de la aplicación del cargador requiere derechos de administrador, por lo que es importante minimizar la frecuencia de actualización del cargador para asegurarse de que los usuarios finales no necesitan elevar con frecuencia, aunque se podría usar Windows Installer revisión de usuario limitada para evitar la elevación de las revisiones del cargador.

Vea el artículo aplicar revisiones a software de juegos en Windows XP, Windows Vista y Windows 7.

### <a name="installation-of-the-game-executables-dlls-and-data"></a>Instalación de los archivos ejecutables del juego, los archivos dll y los datos

Con el fin de facilitar las actualizaciones de usuario estándar del juego sin privilegios administrativos, los archivos ejecutables, dll y datos de los juegos deben instalarse en un área del disco duro que tenga acceso de escritura para todos los usuarios. El sistema operativo proporciona un área "todos los datos de la aplicación" que se puede usar como ubicación predeterminada para la instalación. Se debe usar [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) con la \_ clave AppData común de CSIDL \_ para determinar la ruta de acceso de archivo para esta área. Es importante que no se realice ninguna suposición sobre la ruta de acceso en la que se devuelve esta clave, ya que puede ser configurable por el usuario.

La instalación debe modificar o administrar los permisos de la carpeta para lograr el acceso de escritura todo el usuario necesario para actualizar el título. Con los permisos correctos, la funcionalidad del actualizador de juegos del programa Loader puede revisar fácilmente el juego sin necesidad de tener privilegios especiales de cualquier cuenta de usuarios, incluidas las horas en las que los usuarios estándar lo inician.

### <a name="access-control-list-modification-code"></a>Código de modificación de lista de Access Control

En el caso de Windows XP, deberá ejecutar código para cambiar la lista de control de acceso (ACL) manualmente. esta es una función de ejemplo que muestra cómo hacerlo:

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

Este ejemplo de código también funcionará con Windows Vista y Windows 7; sin embargo, también proporcionan la utilidad de línea de comandos icacls para editar las ACL de archivos que puede usar en su lugar.

La herramienta proporciona una ayuda detallada cuando se ejecuta, pero un uso de ejemplo para la herramienta es:

``` syntax
icacls "C:\Users\All Users\Game" /grant Rex:(D,WDAC)
```

Este uso concederá al usuario los permisos eliminar y escribir DAC en la carpeta Game almacenada en las áreas todos los usuarios de la unidad de disco duro.

### <a name="installations-for-advanced-users"></a>Instalaciones para usuarios avanzados

En escenarios de instalación de usuarios avanzados, es posible que un usuario desee especificar manualmente la ruta de instalación de juegos. La selección de directorio se debe restringir a una parte externa de los archivos de programa para asegurarse de que la carpeta se encuentra en un área verdaderamente compartida del disco duro. La ruta de acceso seleccionada por el usuario solo se debe usar para el archivo exe de juegos y los datos, ya que el cargador de juegos y el programa de instalación de revisión siempre deben instalarse en la carpeta archivos de programa seguros para mejorar la seguridad.

### <a name="the-loaders-verification-of-trust"></a>Comprobación del cargador de confianza

Windows proporciona la función [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust) para comprobar la validez del código firmado y se basa en los servicios criptográficos del sistema operativo. La función está totalmente documentada en MSDN: función **WinVerifyTrust** .

En el siguiente programa de ejemplo de MSDN se detalla el uso de la función para determinar si un ejecutable del programa está firmado con un certificado válido: [ejemplo C programa: comprobar la firma de un archivo PE](/windows/desktop/SecCrypto/example-c-program--verifying-the-signature-of-a-pe-file).

Con el fin de comprobar que el ejecutable del juego firmado es de confianza para ejecutarse desde dentro del cargador, la acción de comprobación genérica será suficiente:

<dl> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valor
</dt> <dd>

\_Acción wintrust \_ genérica \_ Verify \_ V2

</dd> <dt>

<span id="Meaning"></span><span id="meaning"></span><span id="MEANING"></span>Al
</dt> <dd>

Compruebe un archivo o un objeto mediante el proveedor de directivas de Authenticode.

</dd> </dl>

La función toma un argumento de la estructura de entrada que contiene información que el proveedor de confianza necesita para procesar la acción especificada. Normalmente, como en el caso del ejemplo anterior, la estructura incluye información que identifica el objeto que el proveedor de confianza debe evaluar.

El formato de la estructura es específico del identificador de la acción. En el siguiente tema de MSDN se detalla la estructura de ejemplo de la estructura de [**\_ datos**](/windows/desktop/api/wintrust/ns-wintrust-wintrust_data) del proveedor de wintrust: wintrust.

Si el proveedor de confianza comprueba que el sujeto es de confianza para la acción especificada, el valor devuelto es cero. Ningún otro valor además de cero debe considerarse como una devolución correcta.

### <a name="data-validation"></a>Validación de datos

El mecanismo de codiseño solo admite la firma de algunos tipos específicos de archivos, incluidos los ejecutables, los archivos dll, los paquetes de Windows Installer (archivos. msi) y los archivos. cab. La API [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust) no debe usarse para comprobar que los archivos de datos de gran tamaño (por ejemplo, archivos. cab) no se han alterado, ya que hay algunos problemas con el rendimiento y la estabilidad al validar archivos de gran tamaño. Los ejecutables de programas tienden a ser lo suficientemente pequeños como para que se produzca una comprobación de plena confianza mediante el proveedor de WinTrust, pero los archivos de datos de los juegos suelen tener un tamaño de varios gigabytes. El enfoque que toma el cargador para la comprobación de los datos del juego debe ser aquél en el que se prueba una pequeña muestra del conjunto de datos durante el tiempo de ejecución del juego. Este enfoque extiende el costo de las pruebas de comprobación a lo largo de la experiencia de juego y puede proporcionar una experiencia de usuario sin problemas. Para lograrlo, es posible que se requiera una organización cuidadosa de los datos. Algunos MMOGs emplean un enfoque de base de datos para facilitar la administración, el mantenimiento y la comprobación de la corrección de los activos de juego a lo largo del tiempo.

Desde el punto de vista de la seguridad, el código de cliente debe diseñarse para no confiar en los archivos de datos, aunque se use algún tipo de validación de datos básica con el cargador de confianza. Deben emplearse comprobaciones de encabezado, hash y otras comprobaciones de integridad tradicionales. El trabajo para proteger el código de e/s del cliente también debe realizarse mediante técnicas como las pruebas aproximadas, así como aprovechar las herramientas automáticas de análisis de código, como el modificador **/Analyze** en visual Studio 2005 y visual Studio 2008 (disponible en Visual Studio Team System y el compilador gratuito que se incluye con la Windows SDK).

Para obtener más información sobre la seguridad de software, vea [procedimientos de seguridad recomendados para el desarrollo de juegos](/windows/desktop/DxTechArts/best-security-practices-in-game-development).

 

 