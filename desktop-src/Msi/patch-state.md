---
description: La propiedad State devuelve el estado de instalación de esta instancia de patch.
ms.assetid: b01b2839-d867-4353-99d0-8c612cd1eb0c
title: Patch. State (propiedad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.State
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f903ec66c2d55567fee9ccbc123e018e1dc7bacb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653876"
---
# <a name="patchstate-property"></a>Patch. State (propiedad)

La propiedad **State** devuelve el estado de instalación de esta instancia de patch.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Patch.State
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Observaciones

Esta propiedad devuelve uno de los valores siguientes.



| Estado de la instalación        | Significado                                                      |
|---------------------------|--------------------------------------------------------------|
| MSIPATCHSTATE \_ aplicado    | Patch se aplica a esta instancia del producto.                   |
| MSIPATCHSTATE \_ reemplazado | Patch se aplica a esta instancia de producto, pero se reemplaza. |
| MSIPATCHSTATE \_ obsoleto  | La revisión se aplica en esta instancia del producto pero está obsoleta.      |



 

Este método puede devolver ERROR \_ Unknown \_ patch si el objeto [**patch**](patch-object.md) se inicializa con una cadena vacía para *ProductCode*.

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

[**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[No se admite en Windows Installer 2,0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




