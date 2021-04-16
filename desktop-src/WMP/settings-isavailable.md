---
title: Settings. isAvailable
description: La propiedad isAvailable indica si un tipo especificado de información está disponible o se puede realizar una acción especificada. | Settings. isAvailable
ms.assetid: 89403125-545c-482b-a27e-6fee06abe247
keywords:
- Settings. isAvailable Windows Media Player
topic_type:
- apiref
api_name:
- Settings.isAvailable
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a96923fa57ffab4fb2e47b16afd03a06bbffd0ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649753"
---
# <a name="settingsisavailable"></a>Settings. isAvailable

La propiedad **isavailable** indica si un tipo especificado de información está disponible o se puede realizar una acción especificada.

## <a name="syntax"></a>Sintaxis

Player. Settings. isAvailable (nombre)

## <a name="parameters"></a>Parámetros

*name*

Cadena que contiene uno de los valores siguientes.



| String             | Descripción                                                    |
|--------------------|----------------------------------------------------------------|
| AutoStart          | Determina si se puede establecer la propiedad autoStart.          |
| Saldo            | Determina si se puede establecer la propiedad de saldo.            |
| BaseURL            | Determina si se puede establecer la propiedad baseURL.            |
| DefaultFrame       | Determina si se puede establecer la propiedad defaultFrame.       |
| EnableErrorDialogs | Determina si se puede establecer la propiedad enableErrorDialogs. |
| GetMode            | Determina si se puede llamar al método getMode.           |
| InvokeURLs         | Determina si se puede establecer la propiedad invokeURLs.         |
| Silencio               | Determina si se puede establecer la propiedad MUTE.               |
| PlayCount          | Determina si se puede establecer la propiedad playCount.          |
| Tarifa               | Determina si se puede establecer la propiedad Rate.               |
| SetMode            | Determina si se puede llamar al método setMode.           |
| Volumen             | Determina si se puede establecer la propiedad de volumen.             |



 

## <a name="return-values"></a>Valores devueltos

Este método devuelve un valor **booleano** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto de configuración**](settings-object.md)
</dt> </dl>

 

 





