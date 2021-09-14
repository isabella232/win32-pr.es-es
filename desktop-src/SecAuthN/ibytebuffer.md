---
description: La interfaz IByteBuffer se proporciona para leer, escribir y administrar objetos de secuencia. Básicamente, este objeto es un contenedor para el objeto IStream.
ms.assetid: dbc46d53-a421-45c0-a86b-b8a0a212a672
title: Interfaz IByteBuffer (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: dfba15dee78134a9787bf7af994f1d4e2b064339
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160990"
---
# <a name="ibytebuffer-interface"></a>Interfaz IByteBuffer

\[La **interfaz IByteBuffer** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La [**interfaz IStream**](/windows/desktop/api/objidl/nn-objidl-istream) proporciona una funcionalidad similar.\]

La **interfaz IByteBuffer** se proporciona para leer, escribir y administrar objetos de secuencia. Básicamente, este objeto es un contenedor para el **objeto IStream.**

## <a name="members"></a>Members

La **interfaz IByteBuffer** hereda de la [**interfaz IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IByteBuffer** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IByteBuffer** tiene estos métodos.



| Método                                           | Descripción                                                                                               |
|:-------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [**Clonar**](ibytebuffer-clone.md)               | Clona un **objeto IByteBuffer.**<br/>                                                              |
| [**Commit**](ibytebuffer-commit.md)             | Confirma una [*transacción*](/windows/desktop/SecGloss/t-gly).<br/> |
| [**CopyTo**](ibytebuffer-copyto.md)             | Copia bytes en otro objeto.<br/>                                                                |
| [**Inicialización**](ibytebuffer-initialize.md)     | Inicializa el **objeto IByteBuffer.**<br/>                                                        |
| [**LockRegion**](ibytebuffer-lockregion.md)     | Restringe el acceso a un intervalo de bytes.<br/>                                                          |
| [**Lectura**](ibytebuffer-read.md)                 | Lee bytes en la memoria.<br/>                                                                       |
| [**Reversión**](ibytebuffer-revert.md)             | Descarta los cambios desde la última [**llamada commit.**](ibytebuffer-commit.md)<br/>                     |
| [**Seek**](ibytebuffer-seek.md)                 | Cambia el puntero de búsqueda.<br/>                                                                      |
| [**SetSize**](ibytebuffer-setsize.md)           | Cambia el tamaño del objeto de secuencia.<br/>                                                         |
| [**Estadística**](ibytebuffer-stat.md)                 | Recupera información estadística sobre una secuencia.<br/>                                              |
| [**UnlockRegion**](ibytebuffer-unlockregion.md) | Quita la restricción de acceso establecida anteriormente por [**LockRegion**](ibytebuffer-lockregion.md).<br/>     |
| [**Escritura**](ibytebuffer-write.md)               | Escribe bytes en la secuencia.<br/>                                                                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Scardssp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardssp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ IByteBuffer se define como E126F8FE-A7AF-11D0-B88A-00C04FD424B9<br/>          |



 

