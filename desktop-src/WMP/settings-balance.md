---
title: Configuración. saldo
description: La propiedad balance especifica o recupera el equilibrio estéreo actual.
ms.assetid: 26f04989-a1b1-4aec-8a15-c4e3737a4e62
keywords:
- Configuración. saldo de Windows Media Player
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
ms.openlocfilehash: 248cd3b2bbf735ef54382fb5b1be52755cad3799
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649557"
---
# <a name="settingsbalance"></a>Configuración. saldo

La propiedad **balance** especifica o recupera el equilibrio estéreo actual.

## <a name="syntax"></a>Sintaxis

Player. Settings. balance

## <a name="possible-values"></a>Valores posibles

Esta propiedad es un **número** de lectura y escritura (**Long**). Los valores van de 100 a 100, con un valor predeterminado de cero.

## <a name="remarks"></a>Observaciones

El valor cero indica que el audio se reproduce en el mismo volumen en los canales izquierdo y derecho. Un valor de 100 indica que el audio se reproduce solo en el canal izquierdo. Un valor de 100 indica que el audio se reproduce solo en el canal derecho.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto de configuración**](settings-object.md)
</dt> </dl>

 

 





