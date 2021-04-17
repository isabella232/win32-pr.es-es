---
description: La propiedad VerifyDiskSpace es una propiedad de solo lectura.
ms.assetid: 62f11f71-00b0-4e04-8c45-d6d670238886
title: Propiedad Session. VerifyDiskSpace
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
ms.openlocfilehash: a73f2b6f846cb918d5eb10689388a174950c0edc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681120"
---
# <a name="sessionverifydiskspace-property"></a>Propiedad Session. VerifyDiskSpace

La propiedad **VerifyDiskSpace** es una propiedad de solo lectura. Devuelve true si existe suficiente espacio en disco y false si el disco está lleno. Dado que esta propiedad usa la información recopilada por las acciones de costo, solo se debe llamar a **VerifyDiskSpace** después de la acción [CostInitialize](costinitialize-action.md), la [acción FileCost](filecost-action.md)y la [acción CostFinalize](costfinalize-action.md).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Session.VerifyDiskSpace
```



## <a name="property-value"></a>Valor de propiedad

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | El IID \_ ISession se define como 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




