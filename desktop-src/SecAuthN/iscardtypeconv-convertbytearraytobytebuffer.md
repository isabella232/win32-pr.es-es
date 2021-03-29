---
description: Convierte una matriz de bytes de C/C++ típica en un búfer universal de bytes (objeto IStream).
ms.assetid: 512c561a-63f1-463e-9bae-9bec1ebdbe9b
title: 'ISCardTypeConv:: ConvertByteArrayToByteBuffer (método) (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.ConvertByteArrayToByteBuffer
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 406e7aecb7e86802ad67c07669ca199b158ad954
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912457"
---
# <a name="iscardtypeconvconvertbytearraytobytebuffer-method"></a>ISCardTypeConv:: ConvertByteArrayToByteBuffer (método)

\[El método **ConvertByteArrayToByteBuffer** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El método **ConvertByteArrayToByteBuffer** convierte una matriz de bytes de C/C++ típica en un búfer universal de bytes (objeto **IStream** ).

El búfer de bytes creado es un flujo asignado a través de un bloque de memoria. Para obtener acceso al búfer o administrarlo, utilice los métodos proporcionados por la interfaz **IStream** . Una característica única sobre esta implementación de la matriz es que, cuando se llama al método **IStream:: Release** , se liberará la memoria subyacente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ConvertByteArrayToByteBuffer(
  [in]  LPBYTE       pbyArray,
  [in]  DWORD        dwArraySize,
  [out] LPBYTEBUFFER *ppbyBuffer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pbyArray* \[ de\]
</dt> <dd>

Puntero a la matriz de bytes que se va a convertir.

</dd> <dt>

*dwArraySize* \[ de\]
</dt> <dd>

Tamaño de la matriz de bytes que se va a convertir.

</dd> <dt>

*ppbyBuffer* \[ enuncia\]
</dt> <dd>

Puntero al objeto **IStream** que se va a devolver.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles:



| Código devuelto                                                                                   | Descripción                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | Memoria asignada correctamente.<br/>                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Hay un problema con uno o varios de los parámetros pasados a la función.<br/> |
| <dl> <dt>**\_puntero E**</dt> </dl>     | Un parámetro de tipo de puntero era incorrecto.<br/>                                            |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No hay suficiente memoria libre para satisfacer la solicitud.<br/>                                            |



 

## <a name="remarks"></a>Observaciones

La memoria asignada es movible. Use el método **IStream:: Release** para liberar la memoria.

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

 

 
