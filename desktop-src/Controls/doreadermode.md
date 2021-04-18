---
title: DoReaderMode función)
description: Habilita el modo de lector en una ventana.
ms.assetid: 8f898cdd-c907-430a-8287-15d88390c756
keywords:
- DoReaderMode (función) controles de Windows
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
ms.openlocfilehash: d5f5c5863e804cd4bbaab651447e4c6f22dc24a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493354"
---
# <a name="doreadermode-function"></a>DoReaderMode función)

\[**DoReaderMode** está disponible a través de Windows XP con Service Pack 2 (SP2). Puede que no esté disponible en versiones posteriores.\]

Habilita el modo de lector en una ventana.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI DoReaderMode(
  _In_ PREADERMODEINFO prmi
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PRMI* \[ de\]
</dt> <dd>

Tipo: **PREADERMODEINFO**

Puntero a una estructura [**READERMODEINFO**](readermodeinfo.md) que contiene información de inicialización para el modo de lector.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El modo lector se activa a través de los dispositivos compatibles mediante un clic del mouse, normalmente con un tercer botón del mouse o una rueda de desplazamiento. El movimiento del mouse posterior en un área especificada desplaza el contenido de ese área en lugar de mover un puntero. Fuera de ese área, se muestra el puntero del mouse y funciona con normalidad. Un segundo clic del botón o la rueda de desplazamiento libera el dispositivo del modo de lectura.

> [!Note]  
> Esta función no se declara en ningún encabezado público. Para usarlo, debe tener acceso al mismo como ordinal 383 desde Comctl32.dll.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista, \[ solo aplicaciones de escritorio de Windows Vista\]<br/>                                                   |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                            |
| Archivo DLL<br/>                      | <dl> <dt>Comctl32.dll (versión 4,72 o posterior)</dt> </dl> |



 

 





