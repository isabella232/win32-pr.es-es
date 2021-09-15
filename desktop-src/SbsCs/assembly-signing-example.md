---
description: En el ejemplo siguiente se describe cómo generar un ensamblado en paralelo firmado que consta del manifiesto del ensamblado, el catálogo de comprobación y los archivos de ensamblado.
ms.assetid: fa95f292-36e6-4e88-8a0d-aa8bd08def2b
title: Ejemplo de firma de ensamblado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e4c47482074f7decdc44af6b94bc7df31df6969
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127271724"
---
# <a name="assembly-signing-example"></a>Ejemplo de firma de ensamblado

En el ejemplo siguiente se describe cómo generar un ensamblado en paralelo firmado que consta del manifiesto del ensamblado, el catálogo de comprobación y los archivos de ensamblado. Los ensamblados en paralelo compartidos deben estar firmados. El sistema operativo comprueba la firma del ensamblado antes de instalar un ensamblado compartido en el almacén global en paralelo (WinSxS). Esto dificulta la suplantación del publicador del ensamblado en paralelo.

Tenga en cuenta que cambiar los archivos de ensamblado o el contenido del manifiesto después de generar el catálogo de ensamblados invalida el catálogo y el ensamblado. Si debe actualizar los archivos de ensamblado o el manifiesto después de crear y firmar el catálogo, debe firmar de nuevo el ensamblado y generar un nuevo catálogo.

Comience con los archivos de ensamblado, el manifiesto de ensamblado y el archivo de certificado que usará para firmar el ensamblado. El archivo de certificado debe tener 2048 bits o más. No es necesario usar un certificado de confianza. El certificado solo se usa para comprobar que el ensamblado no se ha dañado.

Ejecute la [Pktextract.exe](pktextract-exe.md) que se proporciona en el Kit de desarrollo de software (SDK) de Microsoft Windows para extraer el token de clave pública del archivo de certificado. Para que Pktextract funcione correctamente, el archivo de certificado debe estar presente en el mismo directorio que la utilidad . Use el valor del token de clave pública extraído para actualizar el atributo **publicKeyToken** del **elemento assemblyIdentity** en el archivo de manifiesto.

Este es un ejemplo de un archivo de manifiesto denominado MySampleAssembly.manifest. El ensamblado MySampleAssembly solo contiene un archivo, MYFILE.DLL. Tenga en cuenta que el valor del **atributo publicKeyToken** del elemento **assemblyIdentity** se ha actualizado con el valor del token de clave pública.

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity 
        type="win32" 
        name="Microsoft.Windows.MySampleAssembly" 
        version="1.0.0.0" 
        processorArchitecture="x86"         
        publicKeyToken="0000000000000000"/>
    <file name="myfile.dll"/>
</assembly>
```

A [continuación, ejecuteMt.exe](mt-exe.md) utilidad proporcionada en el SDK Windows. Los archivos de ensamblado deben encontrarse en el mismo directorio que el manifiesto. En este ejemplo, este es el directorio MySampleAssembly. Llame Mt.exe el ejemplo como se muestra a continuación:

**c: \\ MySampleAssembly>mt.exe -manifest MySampleAssembly.manifest -hashupdate -makecdfs**

Este es el aspecto del manifiesto de ejemplo después de ejecutar Mt.exe. Tenga en cuenta que Mt.exe con la opción hashupdate agrega el hash SHA-1 del archivo. No cambie este valor.

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity 
        type="win32" 
        name=" Microsoft.Windows.MySampleAssembly" 
        version="1.0.0.0" 
        processorArchitecture="x86"         
        publicKeyToken="0000000000000000"/>
    <file name="myfile.dll"
hash="a1d362d6278557bbe965a684ac7adb4e57427a29" hashalg="SHA1"/>
</assembly>
```

La Mt.exe con la opción -makecdfs genera un archivo denominado MySampleAssembly.manifest.cdf que describe el contenido del catálogo de seguridad que se usará para validar el manifiesto.

El siguiente paso consiste en ejecutar Makecat.exe este archivo .cdf para crear el catálogo de seguridad para el ensamblado. La llamada a Makecat.exe para este ejemplo aparecería de la siguiente manera:

**c: \\ MySampleAssembly>makecat MySampleAssembly.manifest.cdf**

El último paso consiste en ejecutar SignTool.exe para firmar el archivo de catálogo con el certificado. Debe ser el mismo certificado que se usó en el anterior para generar el token de clave pública. Para obtener más información sobre SignTool.exe vea el [**tema SignTool.**](../seccrypto/signtool.md) La llamada a **SignTool** para el ejemplo aparecería de la siguiente manera:

**c: \\ MySampleAssembly>signtool sign /f \<fullpath> mycompany.pfx /du https: \/ /www.mycompany.com/MySampleAssembly /t https: \/ /timestamp.digicert.com MySampleAssembly.cat**

Si tiene un certificado digital autenticado y la entidad de certificación usa el formato de archivo PVK para almacenar la clave privada, puede usar el importador de archivos de certificado digital PVK (pvkimprt.exe) para importar la clave en el proveedor de servicios criptográficos (CSP). Esta utilidad le permite exportar al formato estándar del sector de PFX/P12. Para obtener más información sobre el importador de archivos de certificado digital PVK, consulte la sección Recursos de implementación de MSDN Library o póngase en contacto con su entidad de certificación. Es posible que pueda obtener pvkimprt.exe de https://office.microsoft.com/downloads/2000/pvkimprt.aspx .

Consulte también Creación [de archivos y catálogos firmados.](creating-signed-files-and-catalogs.md)

 

 
