---
description: Define un método que determina si se permitirá que el shell mueva, copie, elimine o cambie el nombre de una carpeta en la raíz de sincronización de un proveedor de la nube.
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422185"
---
# <a name="istorageprovidercopyhook-interface"></a>Interfaz de IStorageProviderCopyHook

Expone un método que determina si el shell podrá moverse, copiar, eliminar o cambiar el nombre de una carpeta en la raíz de sincronización de un proveedor de la nube.

## <a name="members"></a>Miembros

La interfaz **IStorageProviderCopyHook** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IStorageProviderCopyHook** también tiene estos tipos de miembros:

- [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IStorageProviderCopyHook** tiene estos métodos.



| Método                                           | Descripción                                                                                               |
|:-------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [**CopyCallback**](nf-shobjidl-istorageprovidercopyhook-copycallback.md)               |  Determina si se permitirá que el shell mueva, copie, elimine o cambie el nombre de una carpeta en la raíz de sincronización de un proveedor de nube.                                                           |


## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible | Compilación 19624 de Windows 10 Insider Preview                                                |
| Encabezado<br/>                   | shobjidl. h   |
