---
description: 'Método IEnumMedia::Next: el método Next obtiene el siguiente número especificado de elementos en la secuencia de enumeración.'
ms.assetid: 39c6d082-415f-4375-8cad-6d4c734d277f
title: Método IEnumMedia::Next (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 711e9c844c46aab6ca90988d4e456e926716b201
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113443"
---
# <a name="ienummedianext-method"></a>IEnumMedia::Next (método)

\[ Los controles e interfaces de Conferencia de telefonía IP de Encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método Next** obtiene el siguiente número especificado de elementos en la secuencia de enumeración.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Next(
  [in]  ULONG   celt,
  [out] ITMedia **pVal,
  [out] ULONG   *pceltFetched
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*celta* \[ En\]
</dt> <dd>

Número de elementos solicitados.

</dd> <dt>

*pVal* \[ out\]
</dt> <dd>

Puntero a la [**interfaz ITMedia.**](itmedia.md)

</dd> <dt>

*pceltFetched* \[ out\]
</dt> <dd>

Puntero al número de elementos proporcionados realmente. Puede ser **NULL** si *celta* es uno.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Valor                                                                                     | Significado                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | El método *devolvió el número* de celtas de elementos.<br/>         |
| <dl> <dt>**S \_ FALSE**</dt> </dl>   | El número de elementos restantes era menor *que celta.*<br/> |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl> | El *parámetro pVal* no es un puntero válido.<br/>       |



 

## <a name="remarks"></a>Comentarios

TAPI llama al **método AddRef** en la [**interfaz ITMedia**](itmedia.md) devuelta por **IEnumMedia::Next**. La aplicación debe llamar a **Release** en la **interfaz ITMedia** para liberar recursos asociados a ella.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IEnumMedia**](ienummedia.md)
</dt> </dl>

 

 




