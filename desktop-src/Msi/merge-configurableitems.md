---
description: La propiedad ConfigurableItems de solo lectura del objeto Merge devuelve una colección de objetos ConfigurableItem, cada uno de los cuales representa una sola fila de la tabla ModuleConfiguration.
ms.assetid: 4d1a64f7-fbd0-4358-8911-112e43f1be4a
title: Merge.Configpropiedad urableItems (Mergemod. h)
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
ms.openlocfilehash: 9224aa1cd649971894d78371369b16c6b377cbcc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679455"
---
# <a name="mergeconfigurableitems-property"></a>Merge.Configpropiedad urableItems

La propiedad **ConfigurableItems** de solo lectura del objeto [**Merge**](merge-object.md) devuelve una colección de objetos [**ConfigurableItem**](configurableitem-object.md) , cada uno de los cuales representa una sola fila de la [tabla ModuleConfiguration](moduleconfiguration-table.md). Semánticamente, cada interfaz del enumerador representa un elemento que puede ser configurado por el consumidor del módulo. La colección es una colección de solo lectura e implementa las interfaces de colección estándar de solo lectura de Item (), Count () y \_ NewEnum (). El enumerador **IEnumMsmConfigItems** implementa Next (), SKIP (), RESET () y Clone () con la semántica estándar.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Merge.ConfigurableItems
```



## <a name="property-value"></a>Valor de propiedad

## <a name="c"></a>C++

Consulte [**Get \_ ConfigurableItems**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-get_configurableitems) function.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Mergemod.dll 2,0 o posterior<br/>                                                    |
| Encabezado<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| Archivo DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




