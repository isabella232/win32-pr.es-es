---
description: Proporciona los métodos necesarios para admitir los usuarios de las otras interfaces COM de tarjeta inteligente.
ms.assetid: ce81706b-9201-432e-b9d0-c758769e1040
title: Interfaz ISCardTypeConv (Scarddat. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 8863d29e3ee0f4298410c332329b30fe37dd5048
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909657"
---
# <a name="iscardtypeconv-interface"></a>Interfaz ISCardTypeConv

\[La interfaz **ISCardTypeConv** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

La interfaz **ISCardTypeConv** proporciona los métodos necesarios para admitir los usuarios de las otras interfaces com de [*tarjeta inteligente*](../secgloss/s-gly.md) . Esta interfaz se proporciona solo para la compatibilidad con versiones anteriores y ya no debe usarse.

## <a name="members"></a>Miembros

La interfaz **ISCardTypeConv** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ISCardTypeConv** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ISCardTypeConv** tiene estos métodos.



| Método                                                                              | Descripción                                                                                                                             |
|:------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**ConvertByteArrayToByteBuffer**](iscardtypeconv-convertbytearraytobytebuffer.md) | Convierte una matriz de bytes de C/C++ típica en un búfer universal de bytes (objeto **IStream** ).<br/>                                   |
| [**ConvertByteBufferToByteArray**](iscardtypeconv-convertbytebuffertobytearray.md) | Convierte una matriz de bytes asignada en un búfer universal de bytes (objeto **IStream** ) en una matriz de bytes de C/C++ típica.<br/>          |
| [**ConvertByteBufferToSafeArray**](iscardtypeconv-convertbytebuffertosafearray.md) | Convierte una matriz de bytes asignada en un búfer universal de bytes (objeto **IStream** ) en una SafeArray de char sin signo (byte).<br/> |
| [**ConvertSafeArrayToByteBuffer**](iscardtypeconv-convertsafearraytobytebuffer.md) | Convierte una matriz de bytes definida como SAFEARRAY en un búfer universal de bytes (objeto **IStream** ).<br/>                          |
| [**CreateByteArray**](iscardtypeconv-createbytearray.md)                           | Crea una matriz de bytes.<br/>                                                                                                   |
| [**CreateByteBuffer**](iscardtypeconv-createbytebuffer.md)                         | Crea un búfer universal de bytes asignado en un objeto **IStream** ([**IByteBuffer**](ibytebuffer.md)).<br/>                  |
| [**CreateSafeArray**](iscardtypeconv-createsafearray.md)                           | Crea una matriz SAFEARRAY de automatización de caracteres sin signo (bytes).<br/>                                                              |
| [**FreeIStreamMemoryPtr**](iscardtypeconv-freeistreammemoryptr.md)                 | Libera un puntero de memoria para el bloque de memoria HGLOBAL administrado por una interfaz com **IStream** .<br/>                                  |
| [**GetAtIStreamMemory**](iscardtypeconv-getatistreammemory.md)                     | Adquiere un puntero de byte al bloque de memoria HGLOBAL administrado por la interfaz com **IStream** .<br/>                        |
| [**SizeOfIStream**](iscardtypeconv-sizeofistream.md)                               | Determina el tamaño (número de bytes) de una interfaz com **IStream** .<br/>                                                       |



 

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



 

 
