---
title: How to create an app package signing certificate (Cómo crear un certificado de firma del paquete de la aplicación)
description: Obtenga información sobre cómo usar MakeCert.exe y Pvk2Pfx.exe para crear un certificado de firma de código de prueba, de modo que pueda firmar los paquetes de aplicación de Windows.
ms.assetid: DEDD3727-3F0E-403D-9A6E-55949E98FE74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 382771c23d57b580508017d0bbf24bd742a6eeaf
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077576"
---
# <a name="how-to-create-an-app-package-signing-certificate"></a>How to create an app package signing certificate (Cómo crear un certificado de firma del paquete de la aplicación)

> [!IMPORTANT]
> MakeCert.exe está en desuso. Para obtener instrucciones actuales sobre cómo crear un certificado, consulte [crear un certificado para la firma de paquetes](/windows/msix/package/create-certificate-package-signing).

 

Obtenga información sobre cómo usar [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) y [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) para crear un certificado de firma de código de prueba, de modo que pueda firmar los paquetes de aplicación de Windows.

Debe firmar digitalmente las aplicaciones de Windows empaquetadas antes de implementarlas. Si no usa Microsoft Visual Studio 2012 para crear y firmar los paquetes de la aplicación, debe crear y administrar sus propios certificados de firma de código. Puede crear certificados con [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) y [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) de Windows Driver Kit (WDK). Después, puede usar los certificados para firmar los paquetes de la aplicación, de modo que se puedan implementar localmente para realizar pruebas.

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   [Introducción a la firma de código](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))
-   [Implementación y paquetes de aplicaciones](/previous-versions/windows/apps/hh464929(v=win.10))
-   [Herramientas para firmar controladores](/windows-hardware/drivers/devtest/tools-for-signing-drivers)

### <a name="prerequisites"></a>Requisitos previos

-   Herramientas de [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) y [**Pvk2Pfx.exe**](/windows-hardware/drivers/devtest/pvk2pfx) de WDK

## <a name="instructions"></a>Instrucciones

### <a name="step-1-determine-the-publisher-name-of-the-package"></a>Paso 1: determinar el nombre del publicador del paquete

Para que el certificado de firma que cree se pueda usar con el paquete de la aplicación que desea firmar, el nombre de sujeto del certificado de firma debe coincidir con el atributo **Publisher** del elemento [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) en el AppxManifest.xml de esa aplicación. Por ejemplo, supongamos que el AppxManifest.xml contiene:

``` syntax
  <Identity Name="Contoso.AssetTracker" 
    Version="1.0.0.0" 
    Publisher="CN=Contoso Software, O=Contoso Corporation, C=US"/>
```

Para el parámetro *publisherName* que se especifica con la utilidad [**Makecert**](/windows-hardware/drivers/devtest/makecert) en el paso siguiente, use "CN = contoso software, O = contoso Corporation, C = US".

> [!Note]  
> Esta cadena de parámetro se especifica entre comillas y distingue entre mayúsculas y minúsculas y el espacio en blanco.

 

La cadena de atributo de **publicador** que se define para el elemento [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) en el AppxManifest.xml debe ser idéntica a la cadena que se especifica con el parámetro [**Makecert**](/windows-hardware/drivers/devtest/makecert) /n para el nombre de sujeto del certificado. Copie y pegue la cadena siempre que sea posible.

### <a name="step-2-create-a-private-key-using-makecertexe"></a>Paso 2: creación de una clave privada con MakeCert.exe

Use la utilidad [**Makecert**](/windows-hardware/drivers/devtest/makecert) para crear un certificado de prueba autofirmado y una clave privada:

``` syntax
MakeCert /n publisherName /r /h 0 /eku "1.3.6.1.5.5.7.3.3,1.3.6.1.4.1.311.10.3.13" /e 
expirationDate /sv MyKey.pvk MyKey.cer
```

Este comando le pide que proporcione una contraseña para el archivo. PVK. Le recomendamos que elija una [contraseña segura](/previous-versions/windows/embedded/bb499367(v=winembedded.5)) y que mantenga la clave privada en una ubicación segura.

Se recomienda usar los parámetros sugeridos en el ejemplo anterior por estos motivos:

<dl> <dt>

<span id="_r"></span><span id="_R"></span>**/r**
</dt> <dd>

Crea un certificado raíz autofirmado. Esto simplifica la administración del certificado de prueba.

</dd> <dt>

<span id="_h_0"></span><span id="_H_0"></span>**/h 0**
</dt> <dd>

Marca la restricción básica para el certificado como entidad final. Esto impide que el certificado se use como una entidad de certificación (CA) que pueda emitir otros certificados.

</dd> <dt>

<span id="_eku"></span><span id="_EKU"></span>**/eku**
</dt> <dd>

Establece los valores de uso mejorado de clave (EKU) del certificado.

> [!Note]  
> No incluya un espacio entre los dos valores delimitados por comas.

 

-   1.3.6.1.5.5.7.3.3 indica que el certificado es válido para la firma de código. Especifique siempre este valor para limitar el uso previsto para el certificado.
-   1.3.6.1.4.1.311.10.3.13 indica que el certificado respeta la firma de la duración. Normalmente, si una firma tiene una marca de tiempo, siempre que el certificado sea válido en el momento en que se realizó la marca de tiempo, la firma sigue siendo válida incluso si el certificado expira. Este EKU fuerza la expiración de la firma independientemente de si la firma tiene una marca de tiempo.

</dd> <dt>

<span id="_e"></span><span id="_E"></span>**/e**
</dt> <dd>

Establece la fecha de expiración del certificado. Proporcione un valor para el parámetro *expirationDate* en formato mm/dd/aaaa. Se recomienda elegir una fecha de expiración solo cuando sea necesario para los fines de prueba, normalmente menos de un año. Esta fecha de expiración junto con el EKU de firma de duración puede ayudar a limitar la ventana en la que el certificado puede estar en peligro y usarse inutilizadamente.

</dd> </dl>

Para obtener más información sobre otras opciones, vea [**Makecert**](/windows-hardware/drivers/devtest/makecert).

### <a name="step-3-create-a-personal-information-exchange-pfx-file-using-pvk2pfxexe"></a>Paso 3: crear un archivo de intercambio de información personal (. pfx) mediante Pvk2Pfx.exe

Use la utilidad [**Pvk2Pfx**](/windows-hardware/drivers/devtest/pvk2pfx) para convertir los archivos. PVK y. cer que [**Makecert**](/windows-hardware/drivers/devtest/makecert) creó en un archivo. pfx que puede usar con [SignTool](/windows/desktop/SecCrypto/signtool) para firmar un paquete de aplicación:

``` syntax
Pvk2Pfx /pvk MyKey.pvk /pi pvkPassword /spc MyKey.cer /pfx MyKey.pfx [/po pfxPassword]
```

Los archivos *myKey. PVK* y *myKey. cer* son los mismos archivos que [**MakeCert.exe**](/windows-hardware/drivers/devtest/makecert) creados en el paso anterior. Mediante el parámetro opcional/Po, puede especificar una contraseña diferente para el archivo. pfx resultante. de lo contrario, el archivo. pfx tiene la misma contraseña que *myKey. PVK*.

Para obtener más información sobre otras opciones, vea [**Pvk2Pfx**](/windows-hardware/drivers/devtest/pvk2pfx).

## <a name="remarks"></a>Observaciones

Después de crear el archivo. pfx, puede usar el archivo con [SignTool](/windows/desktop/SecCrypto/signtool) para firmar un paquete de la aplicación. Para obtener más información, consulte [cómo firmar un paquete de aplicación mediante SignTool](how-to-sign-a-package-using-signtool.md). Pero el certificado sigue sin ser de confianza para el equipo local para la implementación de paquetes de aplicaciones hasta que se instala en el almacén de certificados de confianza del equipo local. Puede usar [Certutil.exe](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc732443(v=ws.10)), que viene con Windows.

**Para instalar certificados con WindowsCertutil.exe**

1.  Ejecute **Cmd.exe** como administrador.
2.  Ejecute este comando:

    ``` syntax
    Certutil -addStore TrustedPeople MyKey.cer
    ```

Se recomienda quitar los certificados si ya no están en uso. Desde el mismo símbolo del sistema de administrador, ejecute este comando:

``` syntax
Certutil -delStore TrustedPeople certID
```

**CertID** es el número de serie del certificado. Ejecute este comando para determinar el número de serie del certificado:

``` syntax
Certutil -store TrustedPeople
```

## <a name="security-considerations"></a>Consideraciones sobre la seguridad

Al agregar un certificado a los [almacenes de certificados del equipo local](/windows-hardware/drivers/install/local-machine-and-current-user-certificate-stores), afecta a la confianza del certificado de todos los usuarios del equipo. Se recomienda instalar los certificados de firma de código que desee para probar paquetes de aplicaciones en el almacén de certificados de personas de confianza. Quite los certificados inmediatamente cuando ya no sean necesarios, para evitar que se usen para poner en peligro la confianza del sistema.

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

[How to sign an app package using SignTool](how-to-sign-a-package-using-signtool.md) (Cómo firmar un paquete de la aplicación con SignTool)
</dt> <dt>

[Firma de un paquete de la aplicación](/previous-versions/br230260(v=vs.110))
</dt> </dl>

 

 