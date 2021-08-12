---
title: Configuración.balance
description: La propiedad balance especifica o recupera el saldo estéreo actual.
ms.assetid: 26f04989-a1b1-4aec-8a15-c4e3737a4e62
keywords:
- Configuración.balance Reproductor de Windows Media
topic_type:
- apiref
api_name:
- Settings.balance
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e569c40214655fc643762da8580bd8d6a16e098b99c649bb27e1a1485d498931
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118569580"
---
# <a name="settingsbalance"></a>Configuración.balance

La **propiedad balance** especifica o recupera el saldo estéreo actual.

## <a name="syntax"></a>Syntax

player.settings.balance

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un número de lectura y **escritura** (**long**). Los valores oscilan entre 100 y 100, con un valor predeterminado de cero.

## <a name="remarks"></a>Comentarios

El valor cero indica que el audio se reproduce en el mismo volumen en los canales izquierdo y derecho. Un valor de 100 indica que el audio solo se reproduce en el canal izquierdo. Un valor de 100 indica que el audio solo se reproduce en el canal derecho.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Configuración Objeto**](settings-object.md)
</dt> </dl>

 

 





