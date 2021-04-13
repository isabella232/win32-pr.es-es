---
description: En la tabla MsiPackageCertificate se muestran los certificados de firma digital que se usan para comprobar la identidad de los paquetes de instalación que hacen que esta Multiple-Package la instalación.
ms.assetid: d3a97325-2136-4745-8a7d-57e4d6b9d27e
title: Tabla MsiPackageCertificate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fd39ac93ff24da2fa8334a6e4865172471080b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279338"
---
# <a name="msipackagecertificate-table"></a>Tabla MsiPackageCertificate

En la tabla MsiPackageCertificate se muestran los certificados de firma digital que se usan para comprobar la identidad de los paquetes de instalación que realizan esta [instalación de varios paquetes](multiple-package-installations.md).

Use esta tabla para crear una [instalación de varios paquetes](multiple-package-installations.md) para un producto que contenga varios paquetes de Windows Installer. Si el primer paquete está firmado digitalmente y contiene una tabla MsiPackageCertificate que especifica certificados digitales para todos los paquetes restantes del producto, el administrador solo necesita aceptar el mensaje de [*control de cuentas de usuario*](u-gly.md) (UAC) que se muestra para el primer paquete. Después de aceptar el aviso de UAC para el primer paquete, las funciones definidas por el usuario en la [tabla MsiEmbeddedChainer](msiembeddedchainer-table.md) pueden unir los paquetes restantes a la instalación de varios paquetes sin mostrar un mensaje de UAC y requerir una respuesta de administrador para cada paquete.

Si una o varias de las funciones de la [tabla MsiEmbeddedChainer](msiembeddedchainer-table.md) solicitan un paquete sin firmar, se muestra otro aviso de UAC que requiere la interacción del administrador para cada paquete sin firmar. Si el administrador acepta este aviso de UAC, la instalación de varios paquetes continúa. Una vez que un administrador ha proporcionado las credenciales para un paquete, no se mostrará ningún aviso de UAC para ese paquete durante la instalación de varios paquetes. Si el administrador rechaza un aviso de UAC para un paquete, Windows Installer revierte la instalación de varios paquetes antes de que se confirme para instalar los paquetes que pertenecen al producto.

**[Windows Installer 4,0 o una versión anterior](not-supported-in-windows-installer-4-0.md):** No compatible. Esta tabla está disponible a partir de Windows Installer 4,5.

La tabla MsiPackageCertificate tiene las columnas siguientes:



| Columna               | Tipo                         | Clave | Nullable |
|----------------------|------------------------------|-----|----------|
| PackageCertificate   | [Identificador](identifier.md) | Y   | N        |
| DigitalCertificate\_ | [Identificador](identifier.md) | N   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="PackageCertificate"></span><span id="packagecertificate"></span><span id="PACKAGECERTIFICATE"></span>PackageCertificate
</dt> <dd>

Identificador único de esta fila en la tabla MsiPackageCertificate.

</dd> <dt>

<span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>DigitalCertificate
</dt> <dd>

Una clave externa en la primera columna de la [tabla MsiDigitalCertificate](msidigitalcertificate-table.md). La fila indicada en la tabla MsiDigitalCertificate contiene la representación binaria del certificado del firmante.

</dd> </dl>

## <a name="validation"></a>Validación

<dl>

[ICE39](ice39.md)  
[ICE81](ice81.md)  
</dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[MsiEmbeddedChainer](msiembeddedchainer-table.md)
</dt> <dt>

[Tabla MsiDigitalCertificate](msidigitalcertificate-table.md)
</dt> </dl>

 

 



