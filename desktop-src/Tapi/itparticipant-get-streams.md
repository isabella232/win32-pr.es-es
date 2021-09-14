---
description: El método \_ get Secuencias crea una colección de secuencias asociadas al participante actual.
ms.assetid: 9ab05b14-8ef8-4e7f-b598-05795011e35d
title: Método ITParticipant::get_Streams (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a920929c71e01632edcd8c4c78029b479d8b250
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160641"
---
# <a name="itparticipantget_streams-method"></a>ITParticipant::get \_ Secuencias método

\[**get \_ Secuencias** no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método \_ get Secuencias** crea una colección de secuencias asociadas al participante actual. Este método se proporciona para las aplicaciones cliente de Automation, como las escritas en Visual Basic. Las aplicaciones de C y C++ deben usar [**el método EnumerateStreams.**](itparticipant-enumeratestreams.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Streams(
  [out] VARIANT *pVariant
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pVariant* \[ out\]
</dt> <dd>

Puntero a **VARIANT que** contiene una [**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) de punteros de interfaz [**ITStream.**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Value                                                                                         | Significado                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No existe memoria suficiente para realizar la operación.<br/> |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | El *parámetro pVariant* no es un puntero válido.<br/>     |



 

## <a name="remarks"></a>Observaciones

TAPI llama al **método AddRef** en la [**interfaz ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) devuelta por **ITParticipant::get \_ Secuencias**. La aplicación debe llamar a **Release** en la **interfaz ITStream** para liberar recursos asociados a ella.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|--------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                |
| Encabezado<br/>       | <dl> <dt>Ipmsp.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>  |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ITParticipant**](itparticipant.md)
</dt> <dt>

[**EnumerateStreams**](itparticipant-enumeratestreams.md)
</dt> <dt>

[**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream)
</dt> <dt>

[**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection)
</dt> <dt>

[**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> </dl>

 

