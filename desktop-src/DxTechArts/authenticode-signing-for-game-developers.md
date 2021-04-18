---
title: Firma de Authenticode para desarrolladores de juegos
description: En este artículo se describe cómo empezar a trabajar con la autenticación del juego y cómo integrar la autenticación en un proceso de compilación diario.
ms.assetid: 0b3138ea-e4ea-57fb-756b-62fdc20cf813
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f304e6cc8e185264699709987f62dfdca17bf8b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105665851"
---
# <a name="authenticode-signing-for-game-developers"></a>Firma de Authenticode para desarrolladores de juegos

La autenticación de datos es cada vez más importante para los desarrolladores de juegos. Windows Vista y Windows 7 tienen una serie de características, como controles parentales, que requieren que los juegos estén firmados correctamente para asegurarse de que nadie haya manipulado los datos. Microsoft Authenticode permite a los usuarios finales y al sistema operativo comprobar que el código de programa procede del propietario legítimo y que no se ha modificado o dañado accidentalmente. En este artículo se describe cómo empezar a trabajar con la autenticación del juego y cómo integrar la autenticación en un proceso de compilación diario.

-   [Información preliminar](#background)
-   [Introducción](#getting-started)
-   [Usar una entidad de certificación de confianza](#using-a-trusted-certificate-authority)
-   [Ejemplo de uso de un certificado de prueba](#example-using-a-test-certificate)
-   [Integración del código que inicia sesión en el sistema de compilación diario](#integrating-code-signing-into-the-daily-build-system)
-   [Revocación](#revocation)
-   [Controladores de firma de código](#code-signing-drivers)
-   [Resumen](#summary)
-   [Más información](#more-information)

> [!Note]  
> A partir del 1 de enero de 2016, Windows 7 y versiones posteriores ya no confían en ningún certificado de firma de código SHA-1 con una fecha de expiración del 1 de enero de 2016 o posterior. Para obtener más información [, vea aplicación de Windows de firma de código Authenticode y marcas](https://social.technet.microsoft.com/wiki/contents/articles/32288.windows-enforcement-of-sha1-certificates.aspx) de tiempo.

 

## <a name="background"></a>Información previa

Los certificados digitales se usan para establecer la identidad del autor. Los certificados digitales los emite un tercero de confianza conocido como una entidad de certificación (CA), como VeriSign o Thawte. La entidad de certificación es responsable de comprobar que el propietario no reclama una identificación falsa. Después de aplicar a una entidad de certificación (CA) para un certificado, los desarrolladores comerciales pueden esperar una respuesta a su aplicación en menos de dos semanas.

Después de que la CA decida que cumple sus criterios de Directiva, genera un certificado de firma de código que se ajusta a X. 509, el formato de certificado estándar del sector creado por la Unión Internacional de telecomunicaciones, con las extensiones de la versión 3. Este certificado le identifica y contiene la clave pública. Lo almacena la CA como referencia y se le proporciona una copia electrónicamente. Al mismo tiempo, también se crea una clave privada que debe mantener la seguridad y que no debe compartir con nadie, ni siquiera con la CA.

Una vez que tenga una clave pública y una privada, puede empezar a distribuir el software firmado. Microsoft proporciona herramientas para hacerlo en el Windows SDK. Las herramientas de usan un hash unidireccional, producen un resumen de longitud fija y generan una firma cifrada con una clave privada. A continuación, combinan esa firma cifrada con el certificado y las credenciales en una estructura denominada bloque de firma e incrustarla en el formato de archivo del ejecutable. Se puede firmar cualquier tipo de archivo binario ejecutable, incluidos los archivos dll, los archivos ejecutables y los archivos. cab.

La firma se puede comprobar de varias maneras. Los programas pueden llamar a la función CertVerifyCertificateChainPolicy y se puede usar SignTool (signtool.exe) para comprobar una firma desde el símbolo de la línea de comandos. El explorador de Windows también tiene una pestaña firmas digitales en las propiedades del archivo que muestra cada certificado de un archivo binario firmado. (La pestaña firmas digitales solo aparece en las propiedades de archivo de los archivos firmados.) Además, una aplicación se puede autocomprobar mediante el uso de [**CertVerifyCertificateChainPolicy**](/windows/desktop/api/wincrypt/nf-wincrypt-certverifycertificatechainpolicy).

La firma Authenticode no solo es útil para la autenticación de datos por parte de los usuarios finales, sino que también se necesita para aplicar revisiones de cuentas de usuario limitadas y controles parentales en Windows Vista y Windows 7. Además, las tecnologías futuras de los sistemas operativos Windows también pueden requerir que el código esté firmado, por lo que se recomienda encarecidamente que todos los desarrolladores profesionales y aficionados adquieran un certificado de firma de código de una entidad de certificación. Puede encontrar más información sobre cómo hacerlo más adelante en este artículo sobre el [uso de una entidad de certificación de confianza](#using-a-trusted-certificate-authority).

El código de juego, los evaluadores y los instaladores pueden aprovechar aún más la firma de Authenicode comprobando que los archivos son auténticos en el código. Se puede usar para la protección de la red y la prevención de la seguridad general. Aquí se puede encontrar código de ejemplo para comprobar si un archivo está firmado: [ejemplo de programa C: comprobar la firma de un archivo PE](/windows/desktop/SecCrypto/example-c-program--verifying-the-signature-of-a-pe-file)y ver el código de ejemplo para comprobar la propiedad de un certificado de firma en un archivo firmado: [Cómo obtener información de los ejecutables firmados con Authenticode](https://support.microsoft.com/kb/323809).

## <a name="getting-started"></a>Introducción

Para empezar, Microsoft proporciona herramientas con Visual Studio 2005 y Visual Studio 2008 y, en el [Windows SDK](https://msdn.microsoft.com/windowsserver/bb980924.aspx), para ayudar a realizar y comprobar el proceso de firma de código. Después de instalar Visual Studio o el Windows SDK, las herramientas descritas en este artículo técnico se encuentran en un subdirectorio de la instalación, que puede incluir uno o varios de los siguientes elementos:

-   % SystemDrive% \\ archivos de programa \\ Microsoft Visual Studio 8 \\ SDK \\ v 2.0 \\ bin
-   % SystemDrive% \\ archivos de programa \\ Microsoft Visual Studio 8 \\ VC \\ PlatformSDK \\ bin
-   % SystemDrive% \\ archivos de programa \\ Microsoft Visual Studio 9,0 \\ SmartDevices \\ SDK \\ SDKTools\\
-   % SystemDrive% \\ archivos \\ de programa Microsoft SDK \\ Windows \\ v 6.0 a \\ bin\\

Las siguientes herramientas son las más útiles para firmar código:

<dl> <dt>

<span id="Certificate_Creation_Tool__MakeCert.exe_"></span><span id="certificate_creation_tool__makecert.exe_"></span><span id="CERTIFICATE_CREATION_TOOL__MAKECERT.EXE_"></span>Herramienta de creación de certificados (MakeCert.exe)
</dt> <dd>

Genera un certificado X. 509 de prueba, como un archivo. cer, que contiene la clave pública y una clave privada, como un archivo. PVK. Este certificado solo es para fines de pruebas internas y no se puede usar públicamente.

</dd> <dt>

<span id="pvk2pfx.exe"></span><span id="PVK2PFX.EXE"></span>pvk2pfx.exe
</dt> <dd>

Crea un archivo de intercambio de información personal (. pfx) a partir de un par de archivos. cer y. PVK. El archivo. pfx contiene la clave pública y la privada.

</dd> <dt>

<span id="SignTool__SignTool.exe_"></span><span id="signtool__signtool.exe_"></span><span id="SIGNTOOL__SIGNTOOL.EXE_"></span>SignTool (SignTool.exe)
</dt> <dd>

Firma el archivo con el archivo. pfx. SignTool admite la firma de archivos DLL, archivos ejecutables, archivos de Windows Installer (. msi) y archivos contenedores (. cab).

</dd> </dl>

> [!Note]  
> Al leer otra documentación, es posible que encuentre referencias a SignCode (SignCode.exe), pero esta herramienta está en desuso y ya no se admite; use SignTool en su lugar.

 

## <a name="using-a-trusted-certificate-authority"></a>Usar una entidad de certificación de confianza

Para obtener un certificado de confianza, debe solicitar una entidad de certificación (CA), como VeriSign o Thawte. Microsoft no recomienda ninguna entidad de certificación (CA), pero si desea integrarla en el servicio Informe de errores de Windows (WER), considere la posibilidad de usar VeriSign para emitir el certificado, ya que el acceso a la base de datos WER requiere una cuenta de WinQual que requiera un identificador de VeriSign. Para obtener una lista completa de entidades de certificación de terceros de confianza, vea [miembros del programa de certificados raíz de Microsoft](/previous-versions/ms995347(v=msdn.10)). Para obtener más información acerca del registro con WER, consulte "[Introducción a informe de errores de Windows](https://msdn.microsoft.com/)" en la zona de [ISV](https://msdn.microsoft.com/).

Después de recibir el certificado de la CA, puede firmar el programa mediante SignTool y publicar el programa en el público. Sin embargo, debe tener cuidado de proteger la clave privada, que se encuentra en los archivos. pfx y. PVK. Asegúrese de mantener estos archivos en una ubicación segura.

## <a name="example-using-a-test-certificate"></a>Ejemplo de uso de un certificado de prueba

En los pasos siguientes se muestra la creación de un certificado de firma de código con fines de prueba, seguido de la firma de un programa de ejemplo de Direct3D (llamado BasicHLSL.exe) con este certificado de prueba. Este procedimiento crea archivos. cer y. PVK, que son las claves públicas y privadas, respectivamente, que no se pueden usar para la certificación pública.

En este ejemplo, también se agrega una marca de tiempo a la firma. Una marca de tiempo evita que la firma deje de ser válida cuando el certificado expira. El código que está firmado pero que carece de una marca de tiempo no se validará después de que expire el certificado. Por lo tanto, todo el código publicado públicamente debe tener una marca de tiempo.

**Para crear un certificado y firmar un programa**

1.  Cree un certificado de prueba y una clave privada mediante la herramienta de creación de certificados (MakeCert.exe).

    En el siguiente ejemplo de línea de comandos se especifica MyPrivateKey como nombre de archivo para el archivo de clave privada (. PVK), MyPublicKey como nombre de archivo para el archivo de certificado (. cer) y MySoftwareCompany como nombre del certificado. También hace que el certificado sea autofirmado, para que no tenga una entidad de certificación raíz que no sea de confianza.

    ```
    MakeCert /n CN=MySoftwareCompany /r /h 0 /eku "1.3.6.1.5.5.7.3.3,1.3.6.1.4.1.311.10.3.13" /e 12-31-2020 /sv MyPrivateKey.pvk MyPublicKey.cer
    ```

    

2.  Cree un archivo de intercambio de información personal (. pfx) desde el archivo de clave privada (. PVK) y el archivo de certificado (. cer) mediante pvk2pfx.exe.

    El archivo. pfx combina las claves públicas y privadas en un único archivo. En el siguiente ejemplo de línea de comandos se usan los archivos. PVK y. cer del paso anterior para crear el archivo. pfx denominado MyPFX con la contraseña de la contraseña \_ :

    ```
    pvk2pfx.exe -pvk MyPrivateKey.pvk -spc MyPublicKey.cer -pfx MyPFX.pfx -po your_password
    ```

    

3.  Firme el programa con el archivo de intercambio de información personal (. pfx) mediante SignTool.

    Puede especificar varias opciones en la línea de comandos. En el siguiente ejemplo de línea de comandos se usa el archivo. pfx del paso anterior, se le proporciona la contraseña \_ , se especifica BasicHLSL como el archivo que se va a firmar y se recupera una marca de tiempo de un servidor especificado:

    ```
    signtool.exe sign /fd SHA256 /f MyPFX.pfx /p your_password /v /t URL_to_time_stamp_service BasicHLSL.exe
    ```

    

    > [!Note]  
    > La entidad de certificación proporciona la dirección URL del servicio de marca de tiempo y es opcional para las pruebas. Es importante que la firma de producción incluya una autoridad de marca de tiempo válida, o bien la firma no se validará cuando expire el certificado.

     

4.  Compruebe que el programa está firmado mediante SignTool.

    El siguiente ejemplo de línea de comandos especifica que SignTool debe intentar comprobar la firma en BasicHLSL.exe mediante todos los métodos disponibles a la vez que proporciona una salida detallada:

    ```
    signtool.exe verify /a /v BasicHLSL.exe
    ```

    

    En este ejemplo, SignTool debe indicar que el certificado está asociado, a la vez que indica que no es de confianza, ya que no lo emite una entidad de certificación.

5.  Confíe en el certificado de prueba.

    En el caso de los certificados de prueba, debe confiar en el certificado. Este paso se debe omitir para los certificados proporcionados por una CA, ya que serán de confianza de forma predeterminada.

    En solo los equipos en los que desea confiar en el certificado de prueba, ejecute lo siguiente:

    ```
    certmgr.msc
    ```

    

    A continuación, haga clic con el botón derecho en entidades de certificación raíz de confianza y elija todas las tareas \| Importar. A continuación, busque el archivo. pfx que creó y siga los pasos del asistente y coloque el certificado en las entidades de certificación raíz de confianza.

    Cuando se complete el asistente, podrá iniciar las pruebas con el certificado de confianza en dicho equipo.

## <a name="integrating-code-signing-into-the-daily-build-system"></a>Integración del código que inicia sesión en el sistema de compilación diario

Para integrar la firma de código en un proyecto de, puede crear un archivo por lotes o un script para ejecutar las herramientas de línea de comandos. Una vez compilado el proyecto, ejecute SignTool con la configuración adecuada (como se muestra en el paso 3 de nuestro ejemplo).

Tenga especial cuidado en el proceso de compilación para asegurarse de que el acceso a los archivos. pfx y. PVK está restringido a tantos equipos como usuarios como sea posible. Como procedimiento recomendado, los desarrolladores solo deben firmar el código mediante el certificado de prueba hasta que estén listos para su envío. Una vez más, la clave privada (. PVK) debe mantenerse en una ubicación segura, como una habitación segura o bloqueada, y idealmente en un dispositivo criptográfico, como una tarjeta inteligente.

Se proporciona otro nivel de protección mediante Microsoft Authenticode para firmar el paquete de Windows Installer (MSI). Esto ayuda a proteger el paquete MSI frente a alteraciones y daños accidentales. Consulte la documentación de la herramienta de creación de MSI para obtener más información sobre cómo firmar paquetes con Authenticode.

## <a name="revocation"></a>Revocación

En caso de que la seguridad de la clave privada se vea comprometida o algún evento relacionado con la seguridad presente un Code-Signing certificado no válido, el desarrollador debe revocar el certificado. Si no lo hace, se debilitaría la integridad del desarrollador y la eficacia de firmar el código. Una CA también puede emitir una revocación con hora específica; el código firmado con una marca de tiempo antes del tiempo de revocación se seguirá considerando válido, pero el código con una marca de tiempo subsiguiente no será válido. La revocación de certificados afecta al código de las aplicaciones firmadas con el certificado revocado.

## <a name="code-signing-drivers"></a>Controladores Code-Signing

Los controladores pueden y deben estar firmados con Authenticode. Los controladores en modo kernel tienen requisitos adicionales: las ediciones de 64 bits de Windows Vista y Windows 7 impedirán la instalación de todos los controladores de modo kernel sin firmar y todas las versiones de Windows presentarán un mensaje de advertencia cuando un usuario intente instalar un controlador sin firmar. Además, los administradores pueden establecer directiva de grupo para impedir que se instalen controladores sin firmar en las ediciones Microsoft Windows Server 2003, Windows XP Professional x64 Edition y 32-bit de Windows Vista y Windows 7.

Muchos tipos de controladores pueden estar firmados con una firma de confianza de Microsoft, como parte del programa de certificación de Windows de los [laboratorios de calidad de hardware de Windows](https://www.microsoft.com/whdc/whql/) (WHQL) o el programa de firma no [clasificada](https://www.microsoft.com/whdc/winlogo/drvsign/dqs.mspx) (anteriormente denominado firma de confiabilidad de controladores), que permite al sistema confiar plenamente en estos controladores e instalarlos incluso sin credenciales administrativas.

Como mínimo, los controladores deben estar firmados con Authenticode, ya que los controladores que no están firmados o autofirmados (es decir, que están firmados con un certificado de prueba) no se instalarán en muchas plataformas basadas en Windows. Para obtener más información acerca de la firma de controladores y código y características relacionadas, consulte [requisitos de firma de controladores para Windows](https://www.microsoft.com/whdc/winlogo/drvsign/drvsign.mspx) en el [centro de desarrollo de hardware de Windows](https://www.microsoft.com/whdc/).

## <a name="summary"></a>Resumen

El uso de Microsoft Authenticode es un proceso sencillo. Una vez que haya obtenido una CER y creado una clave privada, se trata de una cuestión sencilla del uso de las herramientas proporcionadas por Microsoft. Después, puede habilitar características importantes en Windows Vista y Windows 7, como el control parental, y permitir que los clientes sepan que el producto procede directamente de su propietario legítimo.

## <a name="more-information"></a>Más información

Para obtener más información sobre las herramientas y los procesos relacionados con la firma de código, vea los vínculos siguientes:

-   [Herramientas de criptografía](/windows/desktop/SecCrypto/cryptography-tools)
-   [Referencia de herramientas de Crypto API](/windows/desktop/SecCrypto/cryptoapi-tools-reference)
-   [Información general sobre Authenticode y turtorials](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537360(v=vs.85))
-   [Certificados digitales](/windows/desktop/SecCrypto/digital-certificates)
-   [Implementar Authenticode](https://www.microsoft.com/technet/security/topics/cryptographyetc/authenticodets.mspx)
-   [Cómo: crear certificados temporales para su uso durante el desarrollo](/dotnet/framework/wcf/feature-details/how-to-create-temporary-certificates-for-use-during-development)

 

 