---
title: Aspectos básicos de almacenamiento estructurado
description: El almacenamiento estructurado proporciona el equivalente de un sistema de archivos completo para almacenar objetos.
ms.assetid: 7e2d6211-2ea0-4cad-9388-c789b12446ab
keywords:
- Strctd de almacenamiento estructurado STG, aspectos fundamentales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d93b74afd620edca5b6beaa43bde6fff43d7263
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904666"
---
# <a name="structured-storage-fundamentals"></a>Aspectos básicos de almacenamiento estructurado

El almacenamiento estructurado proporciona el equivalente de un sistema de archivos completo para almacenar objetos a través de los elementos enumerados en la tabla siguiente.



| Elemento                                                                  | Descripción                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Interfaces de almacenamiento estructurado](structured-storage-interfaces.md)       | Las interfaces [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream), [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)y [**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) , junto con un conjunto de interfaces relacionadas:[**IPersistStorage**](/windows/win32/api/objidl/nn-objidl-ipersiststorage), [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist), [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)y [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream). |
| [Funciones de la API de almacenamiento estructurado](structured-storage-api-functions.md) | API auxiliares que facilitan una implementación de almacenamiento estructurado, así como un segundo conjunto de API para archivos compuestos. es la implementación COM de las interfaces de almacenamiento estructurado. COM también proporciona un conjunto de estructuras y valores de enumeración que se usan para organizar los parámetros de los métodos de interfaz y las API.                              |
| [Modos de acceso de almacenamiento estructurado](structured-storage-access-modes.md)   | Conjunto de modos de acceso para regular el acceso a los archivos compuestos.                                                                                                                                                                                                                                                                                                 |



 

 

 