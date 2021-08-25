---
description: Identifica los posibles certificados de firmante que se usan para firmar digitalmente las revisiones.
ms.assetid: 8f76c27d-92f1-4de7-a69c-fba877e0325d
title: Tabla MsiPatchCertificate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f39d2bc3a05c8b3fe3f23cd7dce01da36e14ce1f3984f24e827606bbc44c1a77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913315"
---
# <a name="msipatchcertificate-table"></a>Tabla MsiPatchCertificate

La tabla MsiPatchCertificate identifica los posibles certificados de firmante que se usan para firmar digitalmente las revisiones. La tabla MsiPatchCertificate contiene la información necesaria para habilitar la aplicación de revisiones de control de cuentas de usuario [(UAC)](user-account-control--uac--patching.md) para una aplicación.

La tabla MsiPatchCertificate tiene las columnas siguientes:



| Columna               | Tipo                         | Clave | Nullable |
|----------------------|------------------------------|-----|----------|
| PatchCertificate     | [Identificador](identifier.md) | Y   | N        |
| DigitalCertificate\_ | [Identificador](identifier.md) | N   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="PatchCertificate"></span><span id="patchcertificate"></span><span id="PATCHCERTIFICATE"></span>PatchCertificate
</dt> <dd>

Identificador único de esta fila en la tabla MsiPatchCertificate.

</dd> <dt>

<span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>DigitalCertificate
</dt> <dd>

Clave externa en la primera columna de [la tabla MsiDigitalCertificate](msidigitalcertificate-table.md). La fila indicada en la tabla MsiDigitalCertificate contiene la representación binaria del certificado de firmante.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Las revisiones siempre se evalúan con respecto a la tabla MsiPatchCertificate actual en el momento en que se aplica la revisión. Una revisión puede modificar la tabla MsiPatchCertificate agregando o quitando entradas. Esto permite que una revisión modifique la evaluación de revisiones futuras que se aplicarán más adelante en la secuencia de aplicación de revisiones. Pueden existir varios certificados en la tabla y la revisión debe coincidir con al menos un certificado que se aplicará.

## <a name="validation"></a>Validación

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE81](ice81.md)  
</dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DisableLUAPatching](disableluapatching.md)
</dt> <dt>

[Revisión de Control de cuentas de usuario (UAC)](user-account-control--uac--patching.md)
</dt> <dt>

[**MSIDISABLELUAPATCHING**](msidisableluapatching.md)
</dt> <dt>

[Instalador de firmas digitales Windows datos](digital-signatures-and-windows-installer.md)
</dt> <dt>

[No se admite en Windows Installer 2.0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



