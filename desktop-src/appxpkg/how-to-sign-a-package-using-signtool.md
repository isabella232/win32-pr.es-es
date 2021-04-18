---
title: Cómo firmar un paquete de la aplicación con SignTool
description: Obtenga información sobre cómo usar SignTool para firmar los paquetes de aplicación de Windows para que se puedan implementar.
ms.assetid: 93541EB4-3419-45D1-AA63-563E6C6D3055
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49f1abfdf0e43fb4d87dbf892f30c2a3ba63e775
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "105705059"
---
# <a name="how-to-sign-an-app-package-using-signtool"></a>Cómo firmar un paquete de la aplicación con SignTool

> [!Note]  
> Para firmar un paquete de aplicación de Windows, consulte [firmar un paquete de aplicación mediante SignTool](/windows/msix/package/sign-app-package-using-signtool).

 

Obtenga información sobre cómo usar [**SignTool**](/windows-hardware/drivers/devtest/signtool) para firmar los paquetes de aplicación de Windows para que se puedan implementar. [**SignTool**](/windows-hardware/drivers/devtest/signtool) forma parte del kit de desarrollo de software (SDK) de Windows.

Todos los paquetes de aplicaciones de Windows deben firmarse digitalmente para poder implementarlos. Aunque Microsoft Visual Studio 2012 y versiones posteriores pueden firmar un paquete de aplicación durante su creación, los paquetes que se crean con la herramienta de [Empaquetador de aplicaciones (MakeAppx.exe)](make-appx-package--makeappx-exe-.md) del Windows SDK no se firman.

> [!Note]  
> Solo puede usar [**SignTool**](/windows-hardware/drivers/devtest/signtool) para firmar los paquetes de aplicación de Windows en Windows 8 y versiones posteriores, o en windows Server 2012 y versiones posteriores. No se puede usar **SignTool** para firmar paquetes de aplicación en sistemas operativos de nivel inferior, como Windows 7 o windows Server 2008 R2.

 

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Introducción a la firma de código](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))
-   [Implementación y paquetes de aplicaciones](/previous-versions/windows/apps/hh464929(v=win.10))
-   [Herramientas para firmar archivos y comprobar firmas](/windows/desktop/SecCrypto/tools-to-sign-files-and-check-signatures)

### <a name="prerequisites"></a>Requisitos previos

-   [**SignTool**](/windows-hardware/drivers/devtest/signtool), que forma parte de la Windows SDK
-   Un certificado de firma de código válido, por ejemplo, un archivo de intercambio de información personal (. pfx) creado con las herramientas de [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) y [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx)

    Para obtener información sobre cómo crear un certificado de firma de código válido, consulte [Cómo crear un certificado de firma de paquete de aplicación](how-to-create-a-package-signing-certificate.md).

-   Una aplicación empaquetada de Windows, por ejemplo, un archivo. appx creado mediante la herramienta de [Empaquetador de aplicaciones (MakeAppx.exe)](make-appx-package--makeappx-exe-.md)

**Consideraciones adicionales**

El certificado que se usa para firmar el paquete de la aplicación debe cumplir estos criterios:

-   El nombre de sujeto del certificado debe coincidir con el atributo de **publicador** que se encuentra en el elemento de [**identidad**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) del archivo de AppxManifest.xml que está almacenado en el paquete. El nombre del publicador forma parte de la identidad de una aplicación de Windows empaquetada, por lo que tiene que hacer que el nombre del firmante del certificado coincida con el nombre del publicador de la aplicación. Esto permite comprobar la identidad de los paquetes firmados con respecto a la firma digital. Para obtener información sobre los errores de firma que pueden surgir al firmar un paquete de aplicación mediante [**SignTool**](/windows-hardware/drivers/devtest/signtool), consulte la sección Comentarios de [Cómo crear un certificado de firma de paquete de aplicación](how-to-create-a-package-signing-certificate.md).
-   El certificado debe ser válido para la firma de código. Esto significa que ambos elementos deben cumplirse:

    -   El campo de uso mejorado de clave (EKU) del certificado debe estar desactivado o contener el valor de EKU para la firma de código (1.3.6.1.5.5.7.3.3).
    -   El campo de uso de clave (KU) del certificado debe estar desactivado o contener el bit de uso de la firma digital (0x80).

-   El certificado contiene una clave privada.
-   El certificado es válido. Está activo, no ha expirado y no se ha revocado.

## <a name="instructions"></a>Instrucciones

### <a name="step-1-determine-the-hash-algorithm-to-use"></a>Paso 1: determinar el algoritmo hash que se va a usar

Al firmar el paquete de la aplicación, debe usar el mismo algoritmo hash que utilizó al crear el paquete de la aplicación. Si ha usado los valores predeterminados para crear el paquete de la aplicación, el algoritmo hash usado es SHA256.

Si usó el Empaquetador de aplicaciones con un algoritmo hash específico para crear el paquete de la aplicación, use el mismo algoritmo para firmar el paquete. Para determinar el algoritmo hash que se va a utilizar para firmar un paquete, puede extraer el contenido del paquete e inspeccionar el archivo de AppxBlockMap.xml. El atributo **HashMethod** del elemento [**BlockMap**](/uwp/schemas/blockmapschema/element-blockmap) indica el algoritmo hash que se usó al crear el paquete de la aplicación. Por ejemplo:

``` syntax
<BlockMap xmlns="http://schemas.microsoft.com/appx/2010/blockmap" 
HashMethod="https://www.w3.org/2001/04/xmlenc#sha256">
```

El elemento [**BlockMap**](/uwp/schemas/blockmapschema/element-blockmap) anterior indica que se ha utilizado el algoritmo SHA256. En esta tabla se muestra la asignación de los algoritmos disponibles actualmente:

| Valor **HashMethod**                            | *hashAlgorithm* que se va a usar |
|-------------------------------------------------|------------------------|
| <https://www.w3.org/2001/04/xmlenc#sha256>       | SHA256 (valor predeterminado de. appx) |
| <https://www.w3.org/2001/04/xmldsig-more#sha384> | SHA384                 |
| <https://www.w3.org/2001/04/xmlenc#sha512>       | SHA512                 |



 

### <a name="step-2-run-signtoolexe-to-sign-the-package"></a>Paso 2: ejecutar SignTool.exe para firmar el paquete

**Para firmar el paquete con un certificado de firma desde un archivo. pfx**

-   ``` syntax
    SignTool sign /fd hashAlgorithm /a /f signingCert.pfx /p password filepath.appx
    ```

[**SignTool**](/windows-hardware/drivers/devtest/signtool) toma como valor predeterminado el parámetro/FD *hashAlgorithm* en SHA1 si no se especifica y SHA1 no es válido para firmar paquetes de aplicaciones. Por lo tanto, debe especificar este parámetro al firmar un paquete de la aplicación. Para firmar un paquete de aplicación que se creó con el hash SHA256 predeterminado, debe especificar el parámetro/FD *hashAlgorithm* como SHA256:

``` syntax
SignTool sign /fd SHA256 /a /f signingCert.pfx /p password filepath.appx
```

Puede omitir el parámetro/p *password* si usa un archivo. pfx que no está protegido por contraseña. También puede usar otras opciones de selección de certificados compatibles con [**SignTool**](/windows-hardware/drivers/devtest/signtool) para firmar paquetes de aplicaciones. Para obtener más información sobre estas opciones, consulte [SignTool](/windows/desktop/SecCrypto/signtool).

> [!Note]  
> No se puede usar la operación de marca de tiempo de [**SignTool**](/windows-hardware/drivers/devtest/signtool) en un paquete de aplicación firmado. la operación no es compatible.

 

Si desea realizar una marca de tiempo en el paquete de la aplicación, debe hacerlo durante la operación de firma. Por ejemplo:

``` syntax
SignTool sign /fd hashAlgorithm /a /f signingCert.pfx /p password /tr timestampServerUrl 
filepath.appx
```

Haga que el parámetro/tr *timestampServerUrl* sea igual a la dirección URL de un servidor de marca de tiempo RFC 3161.

## <a name="remarks"></a>Observaciones

En esta sección se describe la solución de errores de firma para paquetes de aplicaciones.

### <a name="troubleshooting-app-package-signing-errors"></a>Solución de problemas de errores de firma de paquetes de aplicaciones

Además de los errores de firma que [**SignTool**](/windows-hardware/drivers/devtest/signtool) puede devolver, **SignTool** también puede devolver errores específicos de la firma de paquetes de la aplicación. Estos errores suelen aparecer como errores internos:

``` syntax
SignTool Error: An unexpected internal error has occurred.
Error information: "Error: SignerSign() failed." (-2147024885 / 0x8007000B) 
```

Si el código de error comienza con 0x8008, como 0x80080206 APPX \_ E \_ daño en \_ el contenido, indica que el paquete que se está firmando no es válido. En este caso, antes de poder firmar el paquete, debe volver a generar el paquete. Para obtener la lista completa de \* errores de 0x8008, consulte [**códigos de error com (seguridad y configuración)**](/windows/desktop/com/com-error-codes-4).

Lo más habitual es que el error sea 0x8007000b (ERROR de \_ \_ formato incorrecto). En este caso, puede encontrar información de error más específica en el registro de eventos:

**Para buscar en el registro de eventos**

1.  Ejecute eventvwr. msc.
2.  Abra el registro de eventos: Visor de eventos (local) > registros de aplicaciones y servicios > Microsoft > Windows > AppxPackagingOM > Microsoft-Windows-AppxPackaging/Operational
3.  Busque el evento de error más reciente.

El error interno suele corresponder a uno de los siguientes:

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Id. de evento</th>
<th>Ejemplo de cadena de evento</th>
<th>Sugerencia</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>150</td>
<td>error 0x8007000B: el nombre del publicador del manifiesto de la aplicación (CN = contoso) debe coincidir con el nombre del firmante del certificado de firma (CN = Contoso, C = US).</td>
<td>El nombre del publicador del manifiesto de la aplicación debe coincidir exactamente con el nombre de sujeto de la firma.
<blockquote>
[!Note]<br />
Estos nombres se especifican entre comillas y distinguen mayúsculas de minúsculas y espacios en blanco.
</blockquote>
<br/> Puede actualizar la cadena de atributo de <strong>publicador</strong> que se define para el elemento <a href="/uwp/schemas/appxpackage/appxmanifestschema/element-identity"><strong>Identity</strong></a> del archivo AppxManifest.xml para que coincida con el nombre de sujeto del certificado de firma previsto. O bien, seleccione otro certificado de firma con un nombre de sujeto que coincida con el nombre del publicador del manifiesto de la aplicación. El nombre del publicador del manifiesto y el nombre del firmante del certificado se muestran en el mensaje del evento.</td>
</tr>
<tr class="even">
<td>151</td>
<td>error 0x8007000B: el método hash de firma especificado (SHA512) debe coincidir con el método hash usado en la asignación de bloques de paquete de aplicación (SHA256).</td>
<td>El hashAlgorithm especificado en el parámetro/FD es incorrecto (vea el paso 1: determinar el algoritmo hash que se debe usar). Vuelva a ejecutar <a href="/windows-hardware/drivers/devtest/signtool"><strong>SignTool</strong></a> con el hashAlgorithm que coincida con la asignación de bloques del paquete de la aplicación.</td>
</tr>
<tr class="odd">
<td>152</td>
<td>error 0x8007000B: el contenido del paquete de la aplicación debe validarse con su asignación de bloques.</td>
<td>El paquete de la aplicación está dañado y debe volver a generarse para generar una nueva asignación de bloques. Para obtener más información sobre cómo crear un paquete de la aplicación, consulta crear un paquete de la aplicación con el <a href="make-appx-package--makeappx-exe-.md">Empaquetador de aplicaciones</a> o <a href="/previous-versions/hh975357(v=vs.110)">crear un paquete de la aplicación con Visual Studio 2012</a>.</td>
</tr>
</tbody>
</table>



 

## <a name="security-considerations"></a>Consideraciones sobre la seguridad

Una vez firmado el paquete, el certificado que se usó para firmar el paquete todavía debe ser de confianza para el equipo en el que se va a implementar el paquete. Al agregar un certificado a los [almacenes de certificados del equipo local](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores), afecta a la confianza del certificado de todos los usuarios del equipo. Se recomienda que instale los certificados de firma de código que desee para probar paquetes de aplicaciones en el almacén de certificados de personas de confianza y que quite los certificados cuando ya no sea necesario. Si crea sus propios certificados de prueba para firmar paquetes de aplicaciones, también se recomienda restringir los privilegios asociados al certificado de prueba. Para obtener más información sobre cómo crear certificados de prueba para firmar paquetes de aplicaciones, consulte [Cómo crear un certificado de firma de paquete de aplicación](how-to-create-a-package-signing-certificate.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Ejemplos**
</dt> <dt>

[Ejemplo de creación de paquete de aplicación](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/AppxPackingCreateAppx)
</dt> <dt>

**Conceptos**
</dt> <dt>

[Procedimientos recomendados para la firma de código](/previous-versions/windows/hardware/design/dn653556(v=vs.85))
</dt> <dt>

[Firmar un paquete en Visual Studio 2012](/previous-versions/br230260(v=vs.110))
</dt> <dt>

[SignTool](/windows/desktop/SecCrypto/signtool)
</dt> <dt>

[Paquete de aplicaciones (MakeAppx.exe)](make-appx-package--makeappx-exe-.md)
</dt> <dt>

[How to create an app package signing certificate](how-to-create-a-package-signing-certificate.md) (Cómo crear un certificado de firma del paquete de la aplicación)
</dt> </dl>

