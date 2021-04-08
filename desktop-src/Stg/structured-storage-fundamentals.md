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
# <a name="structured-storage-fundamentals"></a><span data-ttu-id="a8d92-104">Aspectos básicos de almacenamiento estructurado</span><span class="sxs-lookup"><span data-stu-id="a8d92-104">Structured Storage Fundamentals</span></span>

<span data-ttu-id="a8d92-105">El almacenamiento estructurado proporciona el equivalente de un sistema de archivos completo para almacenar objetos a través de los elementos enumerados en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="a8d92-105">Structured Storage provides the equivalent of a complete file system for storing objects through the elements listed in the following table.</span></span>



| <span data-ttu-id="a8d92-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="a8d92-106">Element</span></span>                                                                  | <span data-ttu-id="a8d92-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="a8d92-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a8d92-108">Interfaces de almacenamiento estructurado</span><span class="sxs-lookup"><span data-stu-id="a8d92-108">Structured Storage Interfaces</span></span>](structured-storage-interfaces.md)       | <span data-ttu-id="a8d92-109">Las interfaces [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream), [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)y [**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) , junto con un conjunto de interfaces relacionadas:[**IPersistStorage**](/windows/win32/api/objidl/nn-objidl-ipersiststorage), [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist), [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)y [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream).</span><span class="sxs-lookup"><span data-stu-id="a8d92-109">The [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream), [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes), and [**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) interfaces, along with a set of related interfaces —[**IPersistStorage**](/windows/win32/api/objidl/nn-objidl-ipersiststorage), [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist), [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile), and [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream).</span></span> |
| [<span data-ttu-id="a8d92-110">Funciones de la API de almacenamiento estructurado</span><span class="sxs-lookup"><span data-stu-id="a8d92-110">Structured Storage API Functions</span></span>](structured-storage-api-functions.md) | <span data-ttu-id="a8d92-111">API auxiliares que facilitan una implementación de almacenamiento estructurado, así como un segundo conjunto de API para archivos compuestos. es la implementación COM de las interfaces de almacenamiento estructurado.</span><span class="sxs-lookup"><span data-stu-id="a8d92-111">Helper APIs that facilitate an implementation of structured storage, as well as a second set of APIs for compound files; that is the COM implementation of the structured storage interfaces.</span></span> <span data-ttu-id="a8d92-112">COM también proporciona un conjunto de estructuras y valores de enumeración que se usan para organizar los parámetros de los métodos de interfaz y las API.</span><span class="sxs-lookup"><span data-stu-id="a8d92-112">COM also provides a set of supporting structures and enumeration values used to organize parameters for interface methods and APIs.</span></span>                              |
| [<span data-ttu-id="a8d92-113">Modos de acceso de almacenamiento estructurado</span><span class="sxs-lookup"><span data-stu-id="a8d92-113">Structured Storage Access Modes</span></span>](structured-storage-access-modes.md)   | <span data-ttu-id="a8d92-114">Conjunto de modos de acceso para regular el acceso a los archivos compuestos.</span><span class="sxs-lookup"><span data-stu-id="a8d92-114">A set of access modes for regulating access to compound files.</span></span>                                                                                                                                                                                                                                                                                                 |



 

 

 