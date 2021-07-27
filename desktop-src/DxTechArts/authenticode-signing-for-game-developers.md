---
title: Firma de Authenticode para desarrolladores de juegos
description: En este artículo se describe cómo empezar a autenticar el juego y cómo integrar la autenticación en un proceso de compilación diario.
ms.assetid: 0b3138ea-e4ea-57fb-756b-62fdc20cf813
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 256b1cec0693787e76cfa479940524fca28d508e
ms.sourcegitcommit: 5a78723ad484955ac91a23cf282cf9c176c1eab6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/22/2021
ms.locfileid: "114436460"
---
# <a name="authenticode-signing-for-game-developers"></a>Firma de Authenticode para desarrolladores de juegos

La autenticación de datos es cada vez más importante para los desarrolladores de juegos. Windows Vista y Windows 7 tienen una serie de características, como los controles parentales, que requieren que los juegos se firmen correctamente para asegurarse de que nadie haya alterado los datos. Microsoft Authenticode permite a los usuarios finales y al sistema operativo comprobar que el código del programa procede del propietario correcto y que no se ha modificado malintencionadamente ni dañado accidentalmente. En este artículo se describe cómo empezar a autenticar el juego y cómo integrar la autenticación en un proceso de compilación diario.

-   [Información preliminar](#background)
-   [Introducción](#getting-started)
-   [Uso de una entidad de certificación de confianza](#using-a-trusted-certificate-authority)
-   [Ejemplo de uso de un certificado de prueba](#example-using-a-test-certificate)
-   [Integración del inicio de sesión de código en el sistema de compilación diaria](#integrating-code-signing-into-the-daily-build-system)
-   [Revocación](#revocation)
-   [Controladores de firma de código](#code-signing-drivers)
-   [Resumen](#summary)
-   [Más información](#more-information)

> [!Note]  
> A partir del 1 de enero de 2016, Windows 7 y versiones posteriores ya no confían en ningún certificado de firma de código SHA-1 con una fecha de expiración del 1 de enero de 2016 o posterior. Consulte Windows cumplimiento de firma y marca de tiempo de código [authenticode](https://social.technet.microsoft.com/wiki/contents/articles/32288.windows-enforcement-of-sha1-certificates.aspx) para obtener más información.

 

## <a name="background"></a>Fondo

Los certificados digitales se usan para establecer la identidad del autor. Los certificados digitales los emite un tercero de confianza conocido como entidad de certificación (CA), como VeriSign o Thawte. La entidad de certificación es responsable de comprobar que el propietario no está reclamando una identificación falsa. Después de solicitar un certificado a una entidad de certificación, los desarrolladores comerciales pueden esperar una respuesta a su aplicación en menos de dos semanas.

Una vez que la entidad de certificación decide que cumple sus criterios de directiva, genera un certificado de firma de código que se ajusta a X.509, el formato de certificado estándar del sector creado por la Unión internacional de telecomunicaciones, con extensiones de la versión 3. Este certificado le identifica y contiene la clave pública. La entidad de certificación la almacena como referencia y se le entrega una copia electrónicamente. Al mismo tiempo, también crea una clave privada que debe mantener segura y que no debe compartir con nadie, ni siquiera con la entidad de certificación.

Después de tener una clave pública y privada, puede empezar a distribuir software firmado. Microsoft proporciona herramientas para hacerlo en el SDK Windows. Las herramientas usan un hash ungido, generan un resumen de longitud fija y generan una firma cifrada con una clave privada. A continuación, combinan esa firma cifrada con el certificado y las credenciales en una estructura conocida como bloque de firma e insertan en el formato de archivo del archivo ejecutable. Se puede firmar cualquier tipo de archivo binario ejecutable, incluidos archivos DLL, archivos ejecutables y archivos archivadores.

La firma se puede comprobar de varias maneras. Los programas pueden llamar a la función CertVerifyCertificateChainPolicy y SignTool (signtool.exe) se puede usar para comprobar una firma desde el símbolo de la línea de comandos. Windows El Explorador también tiene una pestaña Firmas digitales en Propiedades del archivo que muestra cada certificado de un archivo binario firmado. (La pestaña Firmas digitales solo aparece en Propiedades del archivo para archivos firmados). Además, una aplicación puede realizar la autocertificación mediante [**CertVerifyCertificateChainPolicy**](/windows/desktop/api/wincrypt/nf-wincrypt-certverifycertificatechainpolicy).

La firma authenticode no solo es útil para la autenticación de datos por parte de los usuarios finales, sino que también es necesaria para aplicar revisiones a las cuentas de usuario limitadas y a los controles parentales de Windows Vista y Windows 7. Además, las tecnologías futuras de los sistemas operativos de Windows también pueden requerir que el código esté firmado, por lo que se recomienda encarecidamente que todos los desarrolladores profesionales y profesionales adquieran un certificado de firma de código de una entidad de certificación. Puede encontrar más información sobre cómo hacerlo más adelante en este artículo en Uso de [una entidad de certificación de confianza](#using-a-trusted-certificate-authority).

El código del juego, los patchers y los instaladores pueden aprovechar aún más la firma authenticode comprobando que los archivos son auténticos en el código. Esto se puede usar para la seguridad de red general y anti-cheat. El código de ejemplo para comprobar si un archivo está firmado se puede encontrar aquí: Ejemplo de programa [C:](/windows/desktop/SecCrypto/example-c-program--verifying-the-signature-of-a-pe-file)Comprobar la firma de un archivo PE y código de ejemplo para comprobar la propiedad de un certificado de firma en un archivo firmado se puede encontrar aquí: Cómo obtener información de archivos [ejecutables firmados de Authenticode](https://support.microsoft.com/kb/323809).

## <a name="getting-started"></a>Introducción

Para empezar, Microsoft proporciona herramientas con Visual Studio 2005 y Visual Studio 2008, y en el SDK de [Windows](https://msdn.microsoft.com/windowsserver/bb980924.aspx), para ayudar a realizar y comprobar el proceso de firma de código. Después de instalar Visual Studio o el SDK de Windows, las herramientas descritas en este artículo técnico se encuentran en un subdirectorio de la instalación, que puede incluir uno o varios de los siguientes elementos:

-   %SystemDrive% \\ Archivos de programa Microsoft Visual Studio \\ 8 SDK \\ \\ v2.0 \\ Bin
-   %SystemDrive% \\ Archivos de programa Microsoft Visual Studio \\ 8 VC \\ \\ PlatformSDK \\ Bin
-   %SystemDrive% \\ Archivos de programa Microsoft Visual Studio SDK de \\ SmartDevices 9.0 \\ \\ \\ SdkTools\\
-   %SystemDrive% \\ Archivos de programa sdk de Microsoft Windows bin \\ \\ \\ v6.0A \\\\

Las herramientas siguientes son las más útiles para firmar código:

<dl> <dt>

<span id="Certificate_Creation_Tool__MakeCert.exe_"></span><span id="certificate_creation_tool__makecert.exe_"></span><span id="CERTIFICATE_CREATION_TOOL__MAKECERT.EXE_"></span>Herramienta de creación de certificados (MakeCert.exe)
</dt> <dd>

Genera un certificado X.509 de prueba, como un archivo .cer, que contiene la clave pública y una clave privada, como un archivo .pvk. Este certificado solo tiene fines de prueba interna y no se puede usar públicamente.

</dd> <dt>

<span id="pvk2pfx.exe"></span><span id="PVK2PFX.EXE"></span>pvk2pfx.exe
</dt> <dd>

Crea un archivo de Exchange personal (.pfx) a partir de un par de archivos .cer y .pvk. El archivo .pfx contiene la clave pública y privada.

</dd> <dt>

<span id="SignTool__SignTool.exe_"></span><span id="signtool__signtool.exe_"></span><span id="SIGNTOOL__SIGNTOOL.EXE_"></span>SignTool (SignTool.exe)
</dt> <dd>

Firma el archivo mediante el archivo .pfx. SignTool admite la firma de archivos DLL, archivos ejecutables, archivos Windows Installer (.msi) y archivos de archivo (.cab).

</dd> </dl>

> [!Note]  
> Al leer otra documentación, es posible que encuentre referencias a SignCode (SignCode.exe), pero esta herramienta está en desuso y ya no se admite, use SignTool en su lugar.

 

## <a name="using-a-trusted-certificate-authority"></a>Uso de una entidad de certificación de confianza

Para obtener un certificado de confianza, debe aplicar a una entidad de certificación (CA), como VeriSign o Thawte. Microsoft no recomienda ninguna entidad de certificación sobre otra, pero si desea integrarse en el servicio Informe de errores de Windows (WER), debe considerar el uso de VeriSign para emitir el certificado, ya que el acceso a la base de datos WER requiere una cuenta WinQual que requiere un identificador de VeriSign. Para obtener una lista completa de entidades de certificación de terceros de confianza, vea Miembros del programa de [certificados raíz de Microsoft](/previous-versions/ms995347(v=msdn.10)). Para obtener más información sobre el registro con WER, vea "[Introducing Informe de errores de Windows](https://msdn.microsoft.com/)" in [ISV Zone](https://msdn.microsoft.com/).

Después de recibir el certificado de la entidad de certificación, puede firmar el programa mediante SignTool y publicar el programa al público. Sin embargo, debe tener cuidado de proteger la clave privada, que se encuentra en los archivos .pfx y .pvk. Asegúrese de mantener estos archivos en una ubicación segura.

## <a name="example-using-a-test-certificate"></a>Ejemplo de uso de un certificado de prueba

En los pasos siguientes se muestra la creación de un certificado de firma de código con fines de prueba, seguido de la firma de un programa de ejemplo de Direct3D (denominado BasicHLSL.exe) con este certificado de prueba. Este procedimiento crea archivos .cer y .pvk (las claves públicas y privadas, respectivamente), que no se pueden usar para la certificación pública.

En este ejemplo, también se agrega una marca de tiempo a la firma. Una marca de tiempo impide que la firma no sea válida cuando expira el certificado. El código firmado pero que carece de una marca de tiempo no se validará después de que expire el certificado. Por lo tanto, todo el código publicado públicamente debe tener una marca de tiempo.

**Para crear un certificado y firmar un programa**

1.  Cree un certificado de prueba y una clave privada mediante la herramienta de creación de certificados (MakeCert.exe).

    En el siguiente ejemplo de línea de comandos se especifica MyPrivateKey como nombre de archivo para el archivo de clave privada (.pvk), MyPublicKey como nombre de archivo para el archivo de certificado (.cer) y MySoftwareCompany como nombre del certificado. También hace que el certificado sea autofirmado, de modo que no tenga una entidad raíz que no sea de confianza.

    ```
    MakeCert /n CN=MySoftwareCompany /r /h 0 /eku "1.3.6.1.5.5.7.3.3,1.3.6.1.4.1.311.10.3.13" /e 12-31-2020 /sv MyPrivateKey.pvk MyPublicKey.cer
    ```

    

2.  Cree un archivo de Exchange información personal (.pfx) a partir del archivo de clave privada (.pvk) y el archivo de certificado (.cer) mediante pvk2pfx.exe.

    El archivo .pfx combina las claves públicas y privadas en un único archivo. En el siguiente ejemplo de línea de comandos se usan los archivos .pvk y .cer del paso anterior para crear el archivo .pfx denominado MyPFX con la contraseña de la \_ contraseña:

    ```
    pvk2pfx.exe -pvk MyPrivateKey.pvk -spc MyPublicKey.cer -pfx MyPFX.pfx -po your_password
    ```

    

3.  Firme el programa con el archivo de Exchange personal (.pfx) mediante SignTool.

    Puede especificar varias opciones en la línea de comandos. En el siguiente ejemplo de línea de comandos se usa el archivo .pfx del paso anterior, se proporciona la contraseña como contraseña, se especifica BasicHLSL como archivo que se va a firmar y se recupera una marca de tiempo de un \_ servidor especificado:

    ```
    signtool.exe sign /fd SHA256 /f MyPFX.pfx /p your_password /v /t URL_to_time_stamp_service BasicHLSL.exe
    ```

    

    > [!Note]  
    > La entidad de certificación proporciona la dirección URL al servicio de marca de tiempo y es opcional para las pruebas. Es importante que la firma de producción incluya una entidad de marca de tiempo válida o que la firma no se valide cuando expire el certificado.

     

4.  Compruebe que el programa está firmado mediante SignTool.

    En el ejemplo de línea de comandos siguiente se especifica que SignTool debe intentar comprobar la firma en BasicHLSL.exe mediante todos los métodos disponibles al tiempo que se proporciona una salida detallada:

    ```
    signtool.exe verify /a /v BasicHLSL.exe
    ```

    

    En este ejemplo, SignTool debe indicar que el certificado está asociado, al tiempo que también indica que no es de confianza, ya que no lo emite una CA.

5.  Confíe en el certificado de prueba.

    Para los certificados de prueba, debe confiar en el certificado. Este paso debe omitirse para los certificados proporcionados por una ENTIDAD de certificación, ya que estos confiarán de forma predeterminada.

    En solo los equipos en los que desea confiar en el certificado de prueba, ejecute lo siguiente:

    ```
    certmgr.msc
    ```

    

    A continuación, haga clic con el botón entidades de certificación raíz de confianza y elija Importar todas las \| tareas. A continuación, vaya al archivo .pfx que creó y siga los pasos del asistente, colocando el certificado en el entidades de certificación raíz de confianza.

    Cuando se complete el asistente, puede empezar a probar con el certificado de confianza en ese equipo.

## <a name="integrating-code-signing-into-the-daily-build-system"></a>Integración del inicio de sesión de código en el sistema de compilación diaria

Para integrar el inicio de sesión de código en un proyecto, puede crear un archivo por lotes o un script para ejecutar las herramientas de línea de comandos. Una vez creado el proyecto, ejecute SignTool con la configuración adecuada (como se muestra en el paso 3 de nuestro ejemplo).

Tenga especial cuidado en el proceso de compilación para garantizar que el acceso a los archivos .pfx y .pvk está restringido a tan pocos equipos y usuarios como sea posible. Como procedimiento recomendado, los desarrolladores solo deben firmar código mediante el certificado de prueba hasta que estén listos para enviarse. Una vez más, la clave privada (.pvk) debe mantenerse en una ubicación segura, como una sala segura o bloqueada, e idealmente en un dispositivo criptográfico, como una tarjeta inteligente.

Otra capa de protección se proporciona mediante Microsoft Authenticode para firmar el propio paquete Windows Installer (MSI). Esto ayuda a proteger el paquete MSI contra alteraciones y daños accidentales. Consulte la documentación de la herramienta de creación de MSI para obtener más información sobre cómo firmar paquetes con Authenticode.

## <a name="revocation"></a>Revocación

En caso de que la seguridad de la clave privada se vea comprometida o algún evento relacionado con la seguridad represente un certificado Code-Signing no válido, el desarrollador debe revocar el certificado. Si no lo hace, se desatendría la integridad del desarrollador y la eficacia de firmar el código. Una entidad de certificación también puede emitir una revocación con un tiempo específico; El código firmado con una marca de tiempo anterior a la hora de revocación se seguirá considerando válido, pero el código con una marca de tiempo posterior no será válido. La revocación de certificados afecta al código de las aplicaciones firmadas con el certificado revocado.

## <a name="code-signing-drivers"></a>Code-Signing controladores

Los controladores pueden y deben estar firmados por Authenticode. Los controladores en modo kernel tienen requisitos adicionales: las ediciones de 64 bits de Windows Vista y Windows 7 impedirán la instalación de todos los controladores en modo kernel sin signo y todas las versiones de Windows presentarán un mensaje de advertencia cuando un usuario intente instalar un controlador sin signo. Además, los administradores pueden establecer directiva de grupo para evitar que se instalen controladores sin signo en Microsoft Windows Server 2003, Windows XP Professional x64 Edition y ediciones de 32 bits de Windows Vista y Windows 7.

Muchos tipos de controladores se pueden firmar con una firma de confianza de Microsoft, como parte del Programa de certificación de Windows de [Windows Hardware Quality Labs](https://www.microsoft.com/whdc/whql/) (WHQL) o el Programa de firma sin clasificar (anteriormente denominado Firma de confiabilidad de controladores), que permite al sistema confiar plenamente en estos controladores e instalarlos incluso sin credenciales administrativas. [](https://www.microsoft.com/whdc/winlogo/drvsign/dqs.mspx)

Como mínimo, los controladores deben estar firmados por Authenticode, ya que los controladores sin firmar o autofirmados (es decir, firmados con un certificado de prueba) no se instalarán en muchas plataformas basadas en Windows. Para obtener más información sobre los controladores de firma y el [código](https://www.microsoft.com/whdc/)y la característica relacionada, vea Driver Signing Requirements for [Windows](https://www.microsoft.com/whdc/winlogo/drvsign/drvsign.mspx) on Windows Hardware Developer Central .

## <a name="summary"></a>Resumen

El uso de Microsoft Authenticode es un proceso sencillo. Una vez que haya obtenido una CER y creado una clave privada, es una cuestión sencilla de usar las herramientas proporcionadas por Microsoft. A continuación, puede habilitar características importantes en Windows Vista y Windows 7, como los controles parentales, y hacer que los clientes sepan que el producto procede directamente de su propietario adecuado.

## <a name="more-information"></a>Más información

Para más información sobre las herramientas y los procesos relacionados con la firma de código, consulte los vínculos siguientes:

-   [Herramientas de criptografía](/windows/desktop/SecCrypto/cryptography-tools)
-   [Referencia de herramientas de API de criptografía](/windows/desktop/SecCrypto/cryptoapi-tools-reference)
-   [Información general sobre Authenticode y Vistastoriales](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537360(v=vs.85))
-   [Certificados digitales](/windows/desktop/SecCrypto/digital-certificates)
-   [Implementación de Authenticode](https://www.microsoft.com/technet/security/topics/cryptographyetc/authenticodets.mspx)
-   [Cómo: Crear certificados temporales para usarlos durante el desarrollo](/dotnet/framework/wcf/feature-details/how-to-create-temporary-certificates-for-use-during-development)

 

 
