---
title: Configuración.isAvailable
description: La propiedad isAvailable indica si un tipo especificado de información está disponible o se puede realizar una acción especificada. | Configuración.isAvailable
ms.assetid: 89403125-545c-482b-a27e-6fee06abe247
keywords:
- Configuración.isAvailable Reproductor de Windows Media
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
ms.openlocfilehash: df10026007dd9e04fe88d634a3da566074b0d6a88420ef444d5f2bae39a793fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002415"
---
# <a name="settingsisavailable"></a>Configuración.isAvailable

La **propiedad isAvailable** indica si un tipo especificado de información está disponible o se puede realizar una acción especificada.

## <a name="syntax"></a>Syntax

player.settings.isAvailable( name )

## <a name="parameters"></a>Parámetros

*name*

Cadena que contiene uno de los valores siguientes.



| String             | Descripción                                                    |
|--------------------|----------------------------------------------------------------|
| AutoStart          | Determina si se puede establecer la propiedad autoStart.          |
| Saldo            | Determina si se puede establecer la propiedad de saldo.            |
| Baseurl            | Determina si se puede establecer la propiedad baseURL.            |
| DefaultFrame       | Determina si se puede establecer la propiedad defaultFrame.       |
| EnableErrorDialogs | Determina si se puede establecer la propiedad enableErrorDialogs. |
| GetMode            | Determina si se puede llamar al método getMode.           |
| InvokeURLs         | Determina si se puede establecer la propiedad invokeURLs.         |
| Silencio               | Determina si se puede establecer la propiedad mute.               |
| PlayCount          | Determina si se puede establecer la propiedad playCount.          |
| Tarifa               | Determina si se puede establecer la propiedad rate.               |
| SetMode            | Determina si se puede llamar al método setMode.           |
| Volumen             | Determina si se puede establecer la propiedad del volumen.             |



 

## <a name="return-values"></a>Valores devueltos

Este método devuelve un **valor booleano.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior.<br/>                              |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Configuración Objeto**](settings-object.md)
</dt> </dl>

 

 





