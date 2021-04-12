---
description: Las claves del registro se pueden escribir en el registro del sistema una vez instalados todos los componentes seleccionados y sus archivos relacionados.
ms.assetid: b3b39471-85b1-4361-94fd-19d0f0ee2b78
title: Modificar el registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff6ff79ce340b0487c179cb37e44dff9f42e4be8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361304"
---
# <a name="modifying-the-registry"></a><span data-ttu-id="ed522-103">Modificar el registro</span><span class="sxs-lookup"><span data-stu-id="ed522-103">Modifying the Registry</span></span>

<span data-ttu-id="ed522-104">Las claves del registro se pueden escribir en el registro del sistema una vez instalados todos los componentes seleccionados y sus archivos relacionados.</span><span class="sxs-lookup"><span data-stu-id="ed522-104">Registry keys can be written to the system registry once all selected components and their related files have been installed.</span></span> <span data-ttu-id="ed522-105">Las acciones estándar relacionadas con la modificación del registro se deben secuenciar después de las acciones estándar de instalación de archivos, ya que las claves del registro no se pueden escribir a menos que el componente y el archivo correspondientes se hayan instalado correctamente.</span><span class="sxs-lookup"><span data-stu-id="ed522-105">The standard actions related to modifying the registry must be sequenced after the file installation standard actions because registry keys cannot be written unless the corresponding component and file have been successfully installed.</span></span>

<span data-ttu-id="ed522-106">La [acción RegisterClassInfo](registerclassinfo-action.md) tiene acceso a la [tabla de clases](class-table.md) para registrar la información de clase com de los componentes instalados.</span><span class="sxs-lookup"><span data-stu-id="ed522-106">The [RegisterClassInfo action](registerclassinfo-action.md) accesses the [Class table](class-table.md) to register the COM class information of the installed components.</span></span>

<span data-ttu-id="ed522-107">La [acción RegisterExtensionInfo](registerextensioninfo-action.md) consulta la tabla de [extensión](extension-table.md) y la [tabla de verbos](verb-table.md) y registra las extensiones y la información de verbo de comando correspondientes en el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ed522-107">The [RegisterExtensionInfo action](registerextensioninfo-action.md) queries the [Extension table](extension-table.md) and [Verb table](verb-table.md) and registers the corresponding extensions and command-verb information with the operating system.</span></span>

<span data-ttu-id="ed522-108">La [acción RegisterProgIdInfo](registerprogidinfo-action.md) administra el registro de información de ID. de ensamblado OLE con el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ed522-108">The [RegisterProgIdInfo action](registerprogidinfo-action.md) manages the registration of OLE ProgId information with the operating system.</span></span>

<span data-ttu-id="ed522-109">La [acción RegisterMIMEInfo](registermimeinfo-action.md) procesa la [tabla MIME](mime-table.md) para registrar la asociación entre un tipo de contexto MIME, la extensión de nombre de archivo y el CLSID.</span><span class="sxs-lookup"><span data-stu-id="ed522-109">The [RegisterMIMEInfo action](registermimeinfo-action.md) processes the [MIME table](mime-table.md) to register the association between a MIME context type, the file name extension, and the CLSID.</span></span>

<span data-ttu-id="ed522-110">La [acción WriteRegistryValues](writeregistryvalues-action.md) procesa la [tabla del registro](registry-table.md) y escribe las claves de todos los componentes que se han instalado localmente o que se ejecutan desde el origen.</span><span class="sxs-lookup"><span data-stu-id="ed522-110">The [WriteRegistryValues action](writeregistryvalues-action.md) processes the [Registry table](registry-table.md) and writes the keys for all components that have been either installed locally or to run from source.</span></span> <span data-ttu-id="ed522-111">La tabla del registro permite escribir claves en los subárboles del registro de **\_ las clases HKEY \_ root**, **HKEY \_ Current \_ User**, **HKEY \_ local \_ Machine** y **HKEY \_ users** .</span><span class="sxs-lookup"><span data-stu-id="ed522-111">The Registry table allows keys to be written to the **HKEY\_CLASSES\_ROOT**, **HKEY\_CURRENT\_USER**, **HKEY\_LOCAL\_MACHINE**, and **HKEY\_USERS** registry hives.</span></span>

<span data-ttu-id="ed522-112">La [acción RemoveRegistryValues](removeregistryvalues-action.md) quita las claves que se han marcado para su eliminación en la columna Nombre de la [tabla del registro](registry-table.md) o la [tabla RemoveRegistry](removeregistry-table.md).</span><span class="sxs-lookup"><span data-stu-id="ed522-112">The [RemoveRegistryValues action](removeregistryvalues-action.md) removes the keys that have been marked to be deleted in the Name column of the [Registry table](registry-table.md) or the [RemoveRegistry Table](removeregistry-table.md).</span></span>

<span data-ttu-id="ed522-113">La [acción RegisterTypeLibraries](registertypelibraries-action.md) procesa la [tabla typelib](typelib-table.md) y registra las bibliotecas de tipos instaladas con el sistema.</span><span class="sxs-lookup"><span data-stu-id="ed522-113">The [RegisterTypeLibraries action](registertypelibraries-action.md) processes the [TypeLib table](typelib-table.md) and registers the installed type libraries with the system.</span></span>

 

 



