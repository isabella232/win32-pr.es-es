---
description: La propiedad ConfigurableItems de solo lectura del objeto Merge devuelve una colección De objetos ConfigurableItem, cada uno de los cuales representa una sola fila de la tabla ModuleConfiguration.
ms.assetid: 4d1a64f7-fbd0-4358-8911-112e43f1be4a
title: Merge.Configpropiedad urableItems (Mergemod.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.ConfigurableItems
- IMsmMerge.get_ConfigurableItems
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 179594ba7fe7691edb9abe1f72d104742fe9bc9e3a4a23b728ad8607b94c444a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013043"
---
# <a name="mergeconfigurableitems-property"></a>Merge.Configpropiedad urableItems

La propiedad **ConfigurableItems** de solo lectura del objeto [**Merge**](merge-object.md) devuelve una colección De objetos [**ConfigurableItem,**](configurableitem-object.md) cada uno de los cuales representa una sola fila de la [tabla ModuleConfiguration](moduleconfiguration-table.md). Semánticamente, cada interfaz del enumerador representa un elemento que puede configurar el consumidor del módulo. La colección es una colección de solo lectura e implementa las interfaces de colección de solo lectura estándar de Item(), Count() y \_ NewEnum(). El **enumerador IEnumMsmConfigItems** implementa Next(), Skip(), Reset() y Clone() con la semántica estándar.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Merge.ConfigurableItems
```



## <a name="property-value"></a>Valor de propiedad

## <a name="c"></a>C++

Consulte get ConfigurableItems function (Obtener [**\_ función ConfigurableItems).**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-get_configurableitems)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Mergemod.dll 2.0 o posterior<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| Archivo DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




