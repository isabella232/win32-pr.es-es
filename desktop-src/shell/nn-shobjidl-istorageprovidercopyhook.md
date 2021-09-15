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
ms.openlocfilehash: 52f2a7fb7c8d7b37fc27fd1e91c93d716bc92086
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574528"
---
# <a name="istorageprovidercopyhook-interface"></a>Interfaz de IStorageProviderCopyHook

Expone un método que determina si shell podrá mover, copiar, eliminar o cambiar el nombre de una carpeta en la raíz de sincronización de un proveedor de nube.

## <a name="members"></a>Members

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
| Encabezado<br/>                   | shobjidl.h   |
