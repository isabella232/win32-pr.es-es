---
description: En la tabla MsiPackageCertificate se enumeran los certificados de firma digital que se usan para comprobar la identidad de los paquetes de instalación que hacen que Multiple-Package instalación.
ms.assetid: d3a97325-2136-4745-8a7d-57e4d6b9d27e
title: Tabla MsiPackageCertificate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62abfa23f5e86949d6254ab89f7d70f01a8a4a8fe138a4eba114d2a45559390f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118944523"
---
# <a name="msipackagecertificate-table"></a>Tabla MsiPackageCertificate

En la tabla MsiPackageCertificate se enumeran los certificados de firma digital que se usan para comprobar la identidad de los paquetes de instalación que hacen esta [instalación de varios paquetes.](multiple-package-installations.md)

Use esta tabla para crear una [instalación de varios paquetes](multiple-package-installations.md) para un producto que contenga varios paquetes Windows Installer. Si el primer paquete está firmado digitalmente y contiene una tabla MsiPackageCertificate que especifica certificados digitales para todos los paquetes restantes del producto, el administrador solo debe aceptar el símbolo del sistema de [*Control*](u-gly.md) de cuentas de usuario (UAC) que se muestra para el primer paquete. Después de aceptar el mensaje del UAC para el primer paquete, las funciones definidas por el usuario de la tabla [MsiEmbeddedChainer](msiembeddedchainer-table.md) pueden unir los paquetes restantes a la instalación de varios paquetes sin mostrar un mensaje de UAC y requerir una respuesta de administrador para cada paquete.

Si una o varias de las funciones de la tabla [MsiEmbeddedChainer](msiembeddedchainer-table.md) solicitan un paquete sin signo, se muestra otro mensaje de UAC que requiere la interacción del administrador para cada paquete sin signo. Si el administrador acepta este mensaje de UAC, la instalación de varios paquetes continúa. Una vez que un administrador haya proporcionado las credenciales de un paquete, no se volverá a mostrar ningún mensaje de UAC para ese paquete durante esta instalación de varios paquetes. Si el administrador rechaza un mensaje de UAC para un paquete, el instalador de Windows revierte la instalación de varios paquetes antes de confirmar la instalación de los paquetes que pertenecen al producto.

**[Windows Instalador 4.0 o anterior:](not-supported-in-windows-installer-4-0.md)** No se admite. Esta tabla está disponible a partir de Windows Installer 4.5.

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

Clave externa en la primera columna de [la tabla MsiDigitalCertificate](msidigitalcertificate-table.md). La fila indicada en la tabla MsiDigitalCertificate contiene la representación binaria del certificado de firmante.

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

 

 



