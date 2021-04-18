---
description: La propiedad Format del objeto ConfigurableItem devuelve el valor de la columna Format de la tabla ModuleConfiguration.
ms.assetid: e75ed650-7309-4e24-9c35-82ebf27d011b
title: Propiedad ConfigurableItem. Format (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigurableItem.Format
- IMsmConfigurableItem.get_Format
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 20db09126e9b10aac5c31a3748c4f1606f3f3bab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653625"
---
# <a name="configurableitemformat-property"></a>ConfigurableItem. Format (propiedad)

La propiedad **Format** del objeto [**ConfigurableItem**](configurableitem-object.md) devuelve el valor de la columna Format de la [tabla ModuleConfiguration](moduleconfiguration-table.md).

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = ConfigurableItem.Format
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Observaciones

Esta propiedad solo puede tener los valores siguientes.



| Constante                        | Value |
|---------------------------------|-------|
| **msmConfigurableItemText**     | 0     |
| **msmConfigurableItemKey**      | 1     |
| **msmConfigurableItemInteger**  | 2     |
| **msmConfigurableItemBitfield** | 3     |



 

### <a name="c"></a>C++

Consulte [**Get \_ Format**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfigurableitem-get_format) function.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Mergemod.dll 2,0 o posterior<br/>                                                    |
| Encabezado<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| Archivo DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




