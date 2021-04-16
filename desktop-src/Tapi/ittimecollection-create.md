---
description: El método Create crea un nuevo componente ITTime.
ms.assetid: dee50454-8358-4898-b098-2de51505b658
title: 'ITTimeCollection:: Create (método) (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df62bbc8f1ad2a24a9b80a7f5d0a25bc01f713d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679371"
---
# <a name="ittimecollectioncreate-method"></a>ITTimeCollection:: Create (método)

\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El método **Create** crea un nuevo componente [**ITTime**](ittime.md) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Create(
  [in]  LONG   Index,
  [out] ITTime **ppTime
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Índice* \[ de de\]
</dt> <dd>

Índice del elemento que se va a crear. (La matriz de índice está basada en uno).

</dd> <dt>

*ppTime* \[ enuncia\]
</dt> <dd>

Puntero al componente b creado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Value                                                                                         | Significado                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**\_puntero E**</dt> </dl>     | El parámetro *ppTime* no es un puntero válido.<br/>       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | El parámetro de *Índice* no es válido.<br/>                  |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No hay memoria suficiente para realizar la operación.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Error no especificado.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método aún no se ha implementado.<br/>                  |



 

## <a name="remarks"></a>Observaciones

TAPI llama al método **AddRef** en la interfaz [**ITTime**](ittime.md) devuelta por **ITTimeCollection:: Create**. La aplicación debe llamar a **Release** en la interfaz v para liberar recursos asociados a ella.

Esta función puede enviar datos a través de la conexión en formato no cifrado. por lo tanto, es posible que alguien que escucha en la red pueda leer los datos. El riesgo de seguridad de enviar los datos en texto no cifrado debe tenerse en cuenta antes de usar este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITTimeCollection**](ittimecollection.md)
</dt> <dt>

[**ITTime**](ittime.md)
</dt> </dl>

 

 




