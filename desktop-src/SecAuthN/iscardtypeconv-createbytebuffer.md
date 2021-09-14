---
description: Crea un búfer universal de bytes asignados a un objeto IStream (IByteBuffer).
ms.assetid: 8015c7e8-2cbb-4ba8-9bd0-2f84751840f1
title: Método ISCardTypeConv::CreateByteBuffer (Scarddat.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.CreateByteBuffer
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ab69c8061d2e2740e652e29b2fe6407574fe7076
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127250472"
---
# <a name="iscardtypeconvcreatebytebuffer-method"></a>Método ISCardTypeConv::CreateByteBuffer

\[El **método CreateByteBuffer** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El **método CreateByteBuffer** crea un búfer universal de bytes asignados a un **objeto IStream** [**(IByteBuffer).**](ibytebuffer.md)

El búfer de bytes creado es una secuencia asignada a través de un bloque de memoria. Para acceder al búfer o administrarlo, use los métodos proporcionados por la **interfaz IStream.** Una característica única sobre esta implementación de matriz es que cuando se llama al método **IStream::Release,** se liberará la memoria subyacente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CreateByteBuffer(
  [in]  DWORD        dwAllocSize,
  [out] LPBYTEBUFFER *ppbyBuff
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwAllocSize* \[ En\]
</dt> <dd>

Tamaño en bytes de la memoria que se va a asignar para la matriz.

</dd> <dt>

*ppbyBuff* \[ out\]
</dt> <dd>

Puntero al objeto IStream que se va a devolver.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Los valores devueltos posibles son los siguientes:



| Código devuelto                                                                                   | Descripción                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Memoria asignada correctamente.<br/>                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Hay algún problema con uno o varios de los parámetros pasados a la función.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No hay suficiente memoria libre para satisfacer la solicitud.<br/>                                            |



 

## <a name="remarks"></a>Observaciones

La memoria asignada es móvil. Use el **método IStream::Release** para liberar la memoria.

Para crear una matriz de bytes típica de C/C++, llame a [**CreateByteArray**](iscardtypeconv-createbytearray.md).

Para crear una clase SAFEARRAY de Automation de caracteres sin signo (bytes), llame a [**CreateSafeArray**](iscardtypeconv-createsafearray.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                             |
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

[**CreateByteArray**](iscardtypeconv-createbytearray.md)
</dt> <dt>

[**CreateSafeArray**](iscardtypeconv-createsafearray.md)
</dt> </dl>

 

 
