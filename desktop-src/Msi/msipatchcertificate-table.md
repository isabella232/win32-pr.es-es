---
description: Identifica los posibles certificados de firmante utilizados para firmar digitalmente las revisiones.
ms.assetid: 8f76c27d-92f1-4de7-a69c-fba877e0325d
title: Tabla MsiPatchCertificate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01648e792931fd856a1231a5d876c7db843479df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082778"
---
# <a name="msipatchcertificate-table"></a>Tabla MsiPatchCertificate

La tabla MsiPatchCertificate identifica los posibles certificados de firma que se usan para firmar digitalmente las revisiones. La tabla MsiPatchCertificate contiene la información necesaria para habilitar la aplicación de [revisiones del control de cuentas de usuario (UAC)](user-account-control--uac--patching.md) para una aplicación.

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

Una clave externa en la primera columna de la [tabla MsiDigitalCertificate](msidigitalcertificate-table.md). La fila indicada en la tabla MsiDigitalCertificate contiene la representación binaria del certificado del firmante.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las revisiones siempre se evalúan con respecto a la tabla MsiPatchCertificate que está actualizada en el momento en que se aplica la revisión. Una revisión puede modificar la tabla MsiPatchCertificate agregando o quitando entradas. Esto permite que una revisión modifique la evaluación de revisiones futuras que se aplican posteriormente en la secuencia de aplicación de revisiones. Puede haber varios certificados en la tabla y la revisión debe coincidir con al menos un certificado que se va a aplicar.

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

[Revisión de control de cuentas de usuario (UAC)](user-account-control--uac--patching.md)
</dt> <dt>

[**MSIDISABLELUAPATCHING**](msidisableluapatching.md)
</dt> <dt>

[Firmas digitales y Windows Installer](digital-signatures-and-windows-installer.md)
</dt> <dt>

[No se admite en Windows Installer 2,0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



