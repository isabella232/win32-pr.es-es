---
description: La propiedad VerifyDiskSpace es una propiedad de solo lectura.
ms.assetid: 62f11f71-00b0-4e04-8c45-d6d670238886
title: Propiedad Session.VerifyDiskSpace
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.VerifyDiskSpace
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 4a50bb96088f2c52673fda9a9ddffd786657376bcb4e4a60d5c6d81cb4fbe5e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628765"
---
# <a name="sessionverifydiskspace-property"></a>Propiedad Session.VerifyDiskSpace

La **propiedad VerifyDiskSpace** es una propiedad de solo lectura. Devuelve true si existe suficiente espacio en disco y false si el disco está lleno. Dado que esta propiedad usa la información recopilada por las acciones de cálculo del costo, solo se debe llamar a **VerifyDiskSpace** después de la acción [CostInitialize](costinitialize-action.md), la acción [FileCost](filecost-action.md)y [la acción CostFinalize](costfinalize-action.md).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Session.VerifyDiskSpace
```



## <a name="property-value"></a>Valor de propiedad

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID ISession se define como \_ 000C109E-0000-0000-C000-00000000046<br/>                                                                                                                                                                             |



 

 




