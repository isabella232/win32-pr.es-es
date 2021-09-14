---
description: Libera el puntero de bytes que apunta al bloque de memoria HGLOBAL administrado por una interfaz COM de IStream.
ms.assetid: a76c97a9-d0e9-4eb0-9f97-15f22111187d
title: Método ISCardTypeConv::FreeIStreamMemoryPtr (Scarddat.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.FreeIStreamMemoryPtr
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 12912b8130ed6e1ccaa995f88069b59e96f57c09
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127250466"
---
# <a name="iscardtypeconvfreeistreammemoryptr-method"></a>Método ISCardTypeConv::FreeIStreamMemoryPtr

\[El **método FreeIStreamMemoryPtr** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El **método FreeIStreamMemoryPtr** libera el puntero de bytes que apunta al bloque de memoria HGLOBAL administrado por una interfaz COM **IStream.**

## <a name="syntax"></a>Sintaxis


```C++
HRESULT FreeIStreamMemoryPtr(
  [in] LPSTREAM pStrm,
  [in] LPBYTE   pMem
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pStrm* \[ En\]
</dt> <dd>

Puntero a la **interfaz IStream** que administra el bloque de memoria al que apunta *pMem*.

</dd> <dt>

*pMem* \[ En\]
</dt> <dd>

Puntero al bloque de memoria administrado por la **interfaz IStream.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles:



| Código devuelto                                                                                   | Descripción                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Memoria asignada correctamente.<br/>                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Hay algún problema con uno o varios de los parámetros pasados a la función.<br/> |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | Un parámetro de tipo puntero era incorrecto.<br/>                                            |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No hay suficiente memoria libre para satisfacer la solicitud.<br/>                                            |



 

## <a name="remarks"></a>Observaciones

Esta función libera de forma completa y limpia el puntero de bytes que apunta al bloque de memoria HGLOBAL administrado por la **interfaz IStream.** Una llamada a [**GetAtIStreamMemory**](iscardtypeconv-getatistreammemory.md)adquiere el puntero de bytes.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Scarddat.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scarddat.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID ISCardTypeConv se define como \_ 53B6AA63-3F56-11D0-916B-00AA00C18068<br/>       |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ISCardTypeConv**](iscardtypeconv.md)
</dt> <dt>

[Valores devueltos de tarjeta inteligente](authentication-return-values.md)
</dt> <dt>

[**GetAtIStreamMemory**](iscardtypeconv-getatistreammemory.md)
</dt> </dl>

 

 
