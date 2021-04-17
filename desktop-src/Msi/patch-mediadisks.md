---
description: La propiedad MediaDisks enumera todos los discos multimedia para esta instancia de producto. Esta propiedad llama a MsiSourceListEnumMediaDisks. Devuelve la información del disco como una matriz de objetos de registro.
ms.assetid: 02faf211-16c8-4d2f-b192-c2ce8f3f2c66
title: Patch. MediaDisks (propiedad)
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
ms.openlocfilehash: 40353ecce95cb0c4eb69228b004623bbb87c904e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653364"
---
# <a name="patchmediadisks-property"></a>Patch. MediaDisks (propiedad)

La propiedad **MediaDisks** enumera todos los discos multimedia para esta instancia de producto. Esta propiedad llama a [**MsiSourceListEnumMediaDisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa). Devuelve la información del disco como una matriz de objetos de [**registro**](record-object.md) .

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Patch.MediaDisks
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Observaciones

En cada registro, el primer campo contiene el ID. de disco, el segundo campo contiene la etiqueta de volumen y el tercer campo contiene la solicitud de disco registrada para el disco.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer 3,0 o posterior en Windows Server 2003, Windows XP y Windows 2000<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IPatch se define como 000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Distribución**](patch-object.md)
</dt> <dt>

[**MsiSourceListEnumMediaDisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa)
</dt> <dt>

[**Record**](record-object.md)
</dt> <dt>

[No se admite en Windows Installer 2,0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




