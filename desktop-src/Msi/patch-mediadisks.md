---
description: La propiedad MediaDisks enumera todos los discos multimedia de esta instancia de producto. Esta propiedad llama a MsiSourceListEnumMediaDisks. Devuelve la información de disco como matriz de objetos Record.
ms.assetid: 02faf211-16c8-4d2f-b192-c2ce8f3f2c66
title: Propiedad Patch.MediaDisks
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.MediaDisks
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 462d5b267670804bf2974cf59c848c2684f9e25a07b60488d3a9c0566d89e862
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119558745"
---
# <a name="patchmediadisks-property"></a>Propiedad Patch.MediaDisks

La **propiedad MediaDisks** enumera todos los discos multimedia de esta instancia de producto. Esta propiedad llama a [**MsiSourceListEnumMediaDisks.**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa) Devuelve la información de disco como matriz de [**objetos Record.**](record-object.md)

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Patch.MediaDisks
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Comentarios

En cada registro, el primer campo contiene el identificador de disco, el segundo campo contiene la etiqueta de volumen y el tercer campo contiene la solicitud de disco registrada para el disco.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador 3.0 o posterior en Windows Server 2003, Windows XP y Windows 2000<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID IPatch se define como \_ 000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Parche**](patch-object.md)
</dt> <dt>

[**MsiSourceListEnumMediaDisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa)
</dt> <dt>

[**Registro**](record-object.md)
</dt> <dt>

[No se admite en Windows Installer 2.0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




