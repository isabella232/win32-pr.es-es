---
description: El método Create crea un nuevo componente ITTime.
ms.assetid: dee50454-8358-4898-b098-2de51505b658
title: Método ITTimeCollection::Create (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12a65949d0584f6ed41d3e1611c790b6b94dfa88a4e11ba18818974af5d38cef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117762377"
---
# <a name="ittimecollectioncreate-method"></a>ITTimeCollection::Create (método)

\[Los controles e interfaces de conferencias de telefonía IP de Encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método Create** crea un nuevo componente [**ITTime.**](ittime.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Create(
  [in]  LONG   Index,
  [out] ITTime **ppTime
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Índice* \[ En\]
</dt> <dd>

Índice del elemento que se creará. (La matriz de índices está basada en uno).

</dd> <dt>

*ppTime* \[ out\]
</dt> <dd>

Puntero al componente b creado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Value                                                                                         | Significado                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | El *parámetro ppTime* no es un puntero válido.<br/>       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | El *parámetro Index* no es válido.<br/>                  |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No existe memoria suficiente para realizar la operación.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Error no especificado.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método aún no se ha implementado.<br/>                  |



 

## <a name="remarks"></a>Comentarios

TAPI llama al **método AddRef** en la [**interfaz ITTime**](ittime.md) devuelta por **ITTimeCollection::Create**. La aplicación debe llamar a **Release** en la interfaz v para liberar recursos asociados a ella.

Esta función puede enviar datos a través de la conexión sin cifrar; por lo tanto, alguien que intercepta en la red puede leer los datos. El riesgo de seguridad de enviar los datos en texto sin formato debe tenerse en cuenta antes de usar este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ITTimeCollection**](ittimecollection.md)
</dt> <dt>

[**ITTime**](ittime.md)
</dt> </dl>

 

 




