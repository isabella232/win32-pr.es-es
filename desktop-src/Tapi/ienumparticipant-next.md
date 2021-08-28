---
description: El método Next obtiene el siguiente número especificado de elementos en la secuencia de enumeración. Este método está oculto a los lenguajes Visual Basic y scripting.
ms.assetid: bd94f592-ac6f-48b7-8190-352a5e18f224
title: Método IEnumParticipant::Next (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d574f7c34bc48679ea679caf8ba07c881bcd1c692fa3215ae48a9ecf54d7cbfc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003593"
---
# <a name="ienumparticipantnext-method"></a>IEnumParticipant::Next (Método)

\[**A** continuación, no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método Next** obtiene el siguiente número especificado de elementos en la secuencia de enumeración. Este método está oculto a los lenguajes Visual Basic y scripting.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Next(
  [in]  ULONG         celt,
  [out] ITParticipant **ppElements,
  [out] ULONG         *pceltFetched
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*celta* \[ En\]
</dt> <dd>

Número de elementos solicitados.

</dd> <dt>

*ppElements* \[ out\]
</dt> <dd>

Puntero a [**interfaces ITAgentHandler.**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler)

</dd> <dt>

*pceltFetched* \[ out\]
</dt> <dd>

Puntero al número de elementos proporcionados realmente. Puede ser **NULL** si *celta* es uno.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | El método *devolvió el número* de celtas de elementos.<br/>           |
| <dl> <dt>**S \_ FALSE**</dt> </dl>       | El número de elementos restantes era menor *que celta.*<br/>   |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | El *parámetro ppElements* no es un puntero válido.<br/>   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No existe memoria suficiente para realizar la operación.<br/> |



 

## <a name="remarks"></a>Comentarios

TAPI llama al [**método AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) en la [**interfaz ITAgentHandler**](/windows/win32/api/tapi3cc/nn-tapi3cc-itagenthandler) devuelta por **IEnumParticipant::Next**. La aplicación debe llamar a [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en la **interfaz ITAgentHandler** para liberar recursos asociados a ella.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Header<br/>       | <dl> <dt>Confpriv.h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IEnumParticipant**](ienumparticipant.md)
</dt> <dt>

[**ITParticipant**](itparticipant.md)
</dt> </dl>

 

