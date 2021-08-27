---
title: Cómo firmar un paquete de la aplicación con SignTool
description: Aprenda a usar SignTool para firmar los paquetes Windows aplicación para que se puedan implementar.
ms.assetid: 93541EB4-3419-45D1-AA63-563E6C6D3055
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b4e4c0941cbcced30053b8fd31e44100adc9aa7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474891"
---
# <a name="how-to-sign-an-app-package-using-signtool"></a>Cómo firmar un paquete de la aplicación con SignTool

> [!Note]  
> Para firmar un Windows aplicación, consulte [Firmar un paquete de aplicación mediante SignTool.](/windows/msix/package/sign-app-package-using-signtool)

 

Aprenda a usar [**SignTool para**](/windows-hardware/drivers/devtest/signtool) firmar los paquetes Windows aplicación para que se puedan implementar. [**SignTool**](/windows-hardware/drivers/devtest/signtool) forma parte del kit de desarrollo Windows software (SDK).

Todos Windows paquetes de aplicación deben estar firmados digitalmente antes de poder implementarse. Aunque Microsoft Visual Studio 2012 y versiones posteriores pueden firmar un paquete de aplicación durante su creación, los paquetes que cree mediante la herramienta empaquetador de aplicaciones [(MakeAppx.exe)](make-appx-package--makeappx-exe-.md) del SDK de Windows no están firmados.

> [!Note]  
> Solo puede usar [**SignTool para firmar los**](/windows-hardware/drivers/devtest/signtool) paquetes Windows aplicación en Windows 8 y versiones posteriores o Windows Server 2012 y versiones posteriores. No puede usar **SignTool** para firmar paquetes de aplicación en sistemas operativos de nivel inferior, como Windows 7 o Windows Server 2008 R2.

 

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   [Introducción a la firma de código](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))
-   [Implementación y paquetes de aplicaciones](/previous-versions/windows/apps/hh464929(v=win.10))
-   [Herramientas para firmar archivos y comprobar firmas](/windows/desktop/SecCrypto/tools-to-sign-files-and-check-signatures)

### <a name="prerequisites"></a>Prerrequisitos

-   [**SignTool**](/windows-hardware/drivers/devtest/signtool), que forma parte del SDK de Windows
-   Un certificado de firma de código válido, por ejemplo, un archivo de personal information Exchange (.pfx) creado con las herramientas [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) y [**Pvk2Pfx.exe.**](/windows-hardware/drivers/devtest/pvk2pfx)

    Para obtener información sobre cómo crear un certificado de firma de código válido, [consulte Creación de un certificado de firma de paquete de aplicación.](how-to-create-a-package-signing-certificate.md)

-   Una aplicación Windows empaquetado, por ejemplo, un archivo .appx creado mediante la herramienta [empaquetador de aplicaciones (MakeAppx.exe).](make-appx-package--makeappx-exe-.md)

**Consideraciones adicionales**

El certificado que use para firmar el paquete de aplicación debe cumplir estos criterios:

-   El nombre de sujeto del certificado debe coincidir con el atributo **Publisher** que se encuentra en el elemento [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) del archivo AppxManifest.xml que se almacena en el paquete. El nombre del publicador forma parte de la identidad de una aplicación Windows empaquetada, por lo que debe hacer que el nombre del sujeto del certificado coincida con el nombre del publicador de la aplicación. Esto permite comprobar la identidad de los paquetes firmados con la firma digital. Para obtener información sobre los errores de firma que pueden surgir al firmar un paquete de aplicación mediante [**SignTool**](/windows-hardware/drivers/devtest/signtool), vea la sección Comentarios de Cómo crear un certificado de firma [de paquete de aplicación](how-to-create-a-package-signing-certificate.md).
-   El certificado debe ser válido para la firma de código. Esto significa que ambos elementos deben ser true:

    -   El campo Uso extendido de clave (EKU) del certificado debe estar sin establecer o contener el valor de EKU para la firma de código (1.3.6.1.5.5.7.3.3).
    -   El campo Uso de clave (KU) del certificado debe estar sin establecer o contener el bit de uso para la firma digital (0x80).

-   El certificado contiene una clave privada.
-   El certificado es válido. Está activo, no ha expirado y no se ha revocado.

## <a name="instructions"></a>Instructions

### <a name="step-1-determine-the-hash-algorithm-to-use"></a>Paso 1: Determinar el algoritmo hash que se usará

Al firmar el paquete de aplicación, debe usar el mismo algoritmo hash que usó al crear el paquete de aplicación. Si usó la configuración predeterminada para crear el paquete de aplicación, el algoritmo hash utilizado es SHA256.

Si ha usado el empaquetador de aplicaciones con un algoritmo hash específico para crear el paquete de aplicación, use el mismo algoritmo para firmar el paquete. Para determinar el algoritmo hash que se va a usar para firmar un paquete, puede extraer el contenido del paquete e inspeccionar el AppxBlockMap.xml paquete. El **atributo HashMethod** del [**elemento BlockMap**](/uwp/schemas/blockmapschema/element-blockmap) indica el algoritmo hash que se usó al crear el paquete de aplicación. Por ejemplo:

``` syntax
<BlockMap xmlns="http://schemas.microsoft.com/appx/2010/blockmap" 
HashMethod="https://www.w3.org/2001/04/xmlenc#sha256">
```

El elemento [**BlockMap**](/uwp/schemas/blockmapschema/element-blockmap) anterior indica que se usó el algoritmo SHA256. En esta tabla se muestra la asignación de los algoritmos disponibles actualmente:

| **Valor hashMethod**                            | *hashAlgorithm que se* usará |
|-------------------------------------------------|------------------------|
| <https://www.w3.org/2001/04/xmlenc#sha256>       | SHA256 (valor predeterminado de .appx) |
| <https://www.w3.org/2001/04/xmldsig-more#sha384> | SHA384                 |
| <https://www.w3.org/2001/04/xmlenc#sha512>       | SHA512                 |



 

### <a name="step-2-run-signtoolexe-to-sign-the-package"></a>Paso 2: Ejecutar SignTool.exe para firmar el paquete

**Para firmar el paquete con un certificado de firma desde un archivo .pfx**

-   ``` syntax
    SignTool sign /fd hashAlgorithm /a /f signingCert.pfx /p password filepath.appx
    ```

[**SignTool**](/windows-hardware/drivers/devtest/signtool) establece de forma predeterminada el parámetro /fd *hashAlgorithm* en SHA1 si no se especifica, y SHA1 no es válido para firmar paquetes de aplicación. Por lo tanto, debe especificar este parámetro al firmar un paquete de aplicación. Para firmar un paquete de aplicación que se creó con el hash SHA256 predeterminado, especifique el parámetro /fd *hashAlgorithm* como SHA256:

``` syntax
SignTool sign /fd SHA256 /a /f signingCert.pfx /p password filepath.appx
```

Puede omitir el parámetro /p *password* si usa un archivo .pfx que no está protegido con contraseña. También puede usar otras opciones de selección de certificados compatibles con [**SignTool**](/windows-hardware/drivers/devtest/signtool) para firmar paquetes de aplicación. Para obtener más información sobre estas opciones, [vea SignTool](/windows/desktop/SecCrypto/signtool).

> [!Note]  
> No se puede usar la operación [**de marca de tiempo SignTool**](/windows-hardware/drivers/devtest/signtool) en un paquete de aplicación firmado. No se admite la operación.

 

Si quiere marcar el tiempo del paquete de la aplicación, debe hacerlo durante la operación de firma. Por ejemplo:

``` syntax
SignTool sign /fd hashAlgorithm /a /f signingCert.pfx /p password /tr timestampServerUrl 
filepath.appx
```

Haga que el parámetro /tr *timestampServerUrl* sea igual a la dirección URL de un servidor de marca de tiempo RFC 3161.

## <a name="remarks"></a>Comentarios

En esta sección se describe la solución de problemas de errores de firma para paquetes de aplicaciones.

### <a name="troubleshooting-app-package-signing-errors"></a>Solución de problemas de errores de firma de paquetes de aplicación

Además de los errores de firma que [**SignTool**](/windows-hardware/drivers/devtest/signtool) puede devolver, **SignTool** también puede devolver errores específicos de la firma de paquetes de aplicación. Estos errores suelen aparecer como errores internos:

``` syntax
SignTool Error: An unexpected internal error has occurred.
Error information: "Error: SignerSign() failed." (-2147024885 / 0x8007000B) 
```

Si el código de error comienza con 0x8008, como 0x80080206 CONTENIDO DAÑADO de APPX E), indica que el paquete que se está firmando \_ \_ no es \_ válido. En este caso, para poder firmar el paquete, debe volver a generarlo. Para obtener la lista completa de 0x8008 \* errores, vea [**Códigos de error COM (seguridad y configuración).**](/windows/desktop/com/com-error-codes-4)

Más comúnmente, el error es 0x8007000b (ERROR \_ BAD \_ FORMAT). En este caso, puede encontrar información de error más específica en el registro de eventos:

**Para buscar en el registro de eventos**

1.  Ejecute Eventvwr.msc.
2.  Abra el registro de eventos: Visor de eventos (local) > Applications and Services Logs > Microsoft > Windows > AppxPackagingOM > Microsoft-Windows-AppxPackaging/Operational
3.  Busque el evento de error más reciente.

El error interno suele corresponder a uno de estos:


| Id. de evento | Cadena de evento de ejemplo | Sugerencia | 
|----------|----------------------|------------|
| 150 | error 0x8007000B: el nombre del publicador del manifiesto de aplicación (CN=Contoso) debe coincidir con el nombre del sujeto del certificado de firma (CN=Contoso, C=US). | El nombre del publicador del manifiesto de aplicación debe coincidir exactamente con el nombre de sujeto de la firma.<blockquote>[!Note]<br />Estos nombres se especifican entre comillas y distinguen mayúsculas de minúsculas y espacios en blanco.</blockquote><br /> Puede actualizar la <strong>cadena</strong> Publisher atributo que se define para el elemento <a href="/uwp/schemas/appxpackage/appxmanifestschema/element-identity"><strong>Identity</strong></a> en el archivo AppxManifest.xml para que coincida con el nombre de sujeto del certificado de firma previsto. O bien, seleccione otro certificado de firma con un nombre de sujeto que coincida con el nombre del publicador del manifiesto de aplicación. Tanto el nombre del publicador del manifiesto como el nombre del sujeto del certificado aparecen en el mensaje de evento. | 
| 151 | error 0x8007000B: el método hash de firma especificado (SHA512) debe coincidir con el método hash usado en la asignación de bloques del paquete de aplicación (SHA256). | El hashAlgorithm especificado en el parámetro /fd es incorrecto (vea Paso 1: Determinar el algoritmo hash que se va a usar). Vuelva a ejecutar <a href="/windows-hardware/drivers/devtest/signtool"><strong>SignTool</strong></a> con el hashAlgorithm que coincida con el mapa de bloques del paquete de aplicación. | 
| 152 | error 0x8007000B: el contenido del paquete de aplicación debe validarse con su mapa de bloques. | El paquete de la aplicación está dañado y debe volver a generarse para generar una nueva asignación de bloques. Para obtener más información sobre cómo crear un paquete de aplicación, consulte Creación de un paquete de aplicación con el <a href="make-appx-package--makeappx-exe-.md">empaquetador</a> de aplicaciones o Creación de un paquete de aplicación <a href="/previous-versions/hh975357(v=vs.110)">con Visual Studio 2012</a>. | 




 

## <a name="security-considerations"></a>Consideraciones sobre la seguridad

Una vez firmado el paquete, el certificado que usó para firmar el paquete debe seguir siendo de confianza para el equipo en el que se va a implementar el paquete. Al agregar un certificado a almacenes [de certificados de equipo local,](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores)afecta a la confianza de certificados de todos los usuarios del equipo. Se recomienda instalar los certificados de firma de código que desee para probar paquetes de aplicación en el almacén de certificados de personas de confianza y quitar dichos certificados cuando ya no sean necesarios. Si crea sus propios certificados de prueba para firmar paquetes de aplicación, también se recomienda restringir los privilegios asociados al certificado de prueba. Para obtener más información sobre cómo crear certificados de prueba para firmar paquetes de aplicación, consulte [Creación de un certificado de firma de paquetes de aplicación.](how-to-create-a-package-signing-certificate.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Ejemplos**
</dt> <dt>

[Ejemplo de creación de paquete de aplicación](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/AppxPackingCreateAppx)
</dt> <dt>

**Conceptos**
</dt> <dt>

[Procedimientos recomendados de firma de código](/previous-versions/windows/hardware/design/dn653556(v=vs.85))
</dt> <dt>

[Firma de un paquete en Visual Studio 2012](/previous-versions/br230260(v=vs.110))
</dt> <dt>

[SignTool](/windows/desktop/SecCrypto/signtool)
</dt> <dt>

[Empaquetador de aplicaciones (MakeAppx.exe)](make-appx-package--makeappx-exe-.md)
</dt> <dt>

[How to create an app package signing certificate](how-to-create-a-package-signing-certificate.md) (Cómo crear un certificado de firma del paquete de la aplicación)
</dt> </dl>

