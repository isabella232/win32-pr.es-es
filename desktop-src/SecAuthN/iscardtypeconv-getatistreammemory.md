---
description: Adquiere un puntero de byte al bloque de memoria HGLOBAL administrado por la interfaz COM IStream.
ms.assetid: ea25eb98-b841-4f5e-b428-3d9cb8176142
title: 'ISCardTypeConv:: GetAtIStreamMemory (método) (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.GetAtIStreamMemory
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: bdd828921f18c3d06edd2d41da189260a4ed4394
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808677"
---
# <a name="iscardtypeconvgetatistreammemory-method"></a>ISCardTypeConv:: GetAtIStreamMemory (método)

\[El método **GetAtIStreamMemory** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El método **GetAtIStreamMemory** adquiere un puntero de byte al bloque de memoria hglobal administrado por la interfaz com **IStream** .

Se trata de una manera de obtener la memoria en la **IStream** sin tener que obtener el valor sizeof para el bloque de memoria en bytes y leer los bytes en una matriz de bytes temporal mediante la interfaz **IStream** .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetAtIStreamMemory(
  [in]  LPSTREAM    pStrm,
  [out] LPBYTEARRAY *ppMem
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pStrm* \[ de\]
</dt> <dd>

Puntero a la interfaz com **IStream** que administra el bloque de memoria hglobal.

</dd> <dt>

*ppMem* \[ enuncia\]
</dt> <dd>

Puntero al primer byte del bloque de memoria HGLOBAL si se realiza correctamente; en caso contrario, **null** si se produce un error en la operación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles.



| Código devuelto                                                                                   | Descripción                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | Memoria asignada correctamente.<br/>                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Hay un problema con uno o varios de los parámetros pasados a la función.<br/> |
| <dl> <dt>**\_puntero E**</dt> </dl>     | Un parámetro de tipo de puntero era incorrecto.<br/>                                            |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No hay suficiente memoria libre para satisfacer la solicitud.<br/>                                            |



 

## <a name="remarks"></a>Observaciones

El recuento de referencias de **IStream** se incrementará para cada puntero *ppMem* adquirido.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Scarddat. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scarddat. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardTypeConv se define como 53B6AA63-3F56-11D0-916B-00AA00C18068<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ISCardTypeConv**](iscardtypeconv.md)
</dt> <dt>

[Valores devueltos de tarjeta inteligente](authentication-return-values.md)
</dt> </dl>

 

 
