---
description: Define un método que determina si shell podrá mover, copiar, eliminar o cambiar el nombre de una carpeta en la raíz de sincronización de un proveedor de nube.
title: Interfaz de IStorageProviderCopyHook
ms.topic: reference
ms.date: 11/11/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- IStorageProviderCopyHook
api_type:
- COM
api_location:
- shobjidl.h
ms.openlocfilehash: aa26a329bd80295a6a46a1bb11d1dc651baf1ea71975576ed704b29a7fee8b57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968874"
---
# <a name="istorageprovidercopyhook-interface"></a>Interfaz de IStorageProviderCopyHook

Expone un método que determina si shell podrá mover, copiar, eliminar o cambiar el nombre de una carpeta en la raíz de sincronización de un proveedor de nube.

## <a name="members"></a>Miembros

La **interfaz IStorageProviderCopyHook** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IStorageProviderCopyHook** también tiene estos tipos de miembros:

- [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IStorageProviderCopyHook** tiene estos métodos.



| Método                                           | Descripción                                                                                               |
|:-------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [**CopyCallback**](nf-shobjidl-istorageprovidercopyhook-copycallback.md)               |  Determina si shell podrá mover, copiar, eliminar o cambiar el nombre de una carpeta en la raíz de sincronización de un proveedor de nube.                                                           |


## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible | Windows 10 Insider Preview Build 19624                                                |
| Header<br/>                   | shobjidl.h   |
