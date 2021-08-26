---
title: Función DoReaderMode
description: Habilita el modo lector en una ventana.
ms.assetid: 8f898cdd-c907-430a-8287-15d88390c756
keywords:
- Controles de Windows doReaderMode
topic_type:
- apiref
api_name:
- DoReaderMode
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63b71538e41e4b70155da8352e531b620fbe5de7f62746713c3a2a58f3adddf2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002695"
---
# <a name="doreadermode-function"></a>Función DoReaderMode

\[**DoReaderMode** está disponible a través Windows XP con Service Pack 2 (SP2). Es posible que no esté disponible en versiones posteriores.\]

Habilita el modo lector en una ventana.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI DoReaderMode(
  _In_ PREADERMODEINFO prmi
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*prmi* \[ En\]
</dt> <dd>

Tipo: **PREADERMODEINFO**

Puntero a una estructura [**READERMODEINFO**](readermodeinfo.md) que contiene información de inicialización para el modo de lector.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

El modo lector se activa a través de dispositivos compatibles mediante un clic del mouse, normalmente con un tercer botón del mouse o rueda de desplazamiento. El movimiento posterior del mouse en un área especificada desplaza el contenido de esa área en lugar de mover un puntero. Fuera de esa área, se muestra el puntero del mouse y funciona con normalidad. Un segundo clic del botón o la rueda de desplazamiento libera el dispositivo del modo de lector.

> [!Note]  
> Esta función no se declara en ningún encabezado público. Para usarlo, debe acceder a él como ordinal 383 desde Comctl32.dll.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista, solo Windows aplicaciones \[ de escritorio de Vista\]<br/>                                                   |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                            |
| Archivo DLL<br/>                      | <dl> <dt>Comctl32.dll (versión 4.72 o posterior)</dt> </dl> |



 

 





