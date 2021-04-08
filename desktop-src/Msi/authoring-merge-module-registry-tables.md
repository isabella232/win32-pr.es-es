---
description: Use tablas del registro del módulo de mezcla según el tipo de información del registro.
ms.assetid: 091429ff-a8f4-4e1b-929f-1559cd173c3d
title: Crear tablas del registro del módulo de combinación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d10e31ac82d190c87019da5bc77408b58122a523
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001729"
---
# <a name="authoring-merge-module-registry-tables"></a><span data-ttu-id="b5f8b-103">Crear tablas del registro del módulo de combinación</span><span class="sxs-lookup"><span data-stu-id="b5f8b-103">Authoring Merge Module Registry Tables</span></span>

<span data-ttu-id="b5f8b-104">Use tablas del registro del módulo de mezcla según el tipo de información del registro.</span><span class="sxs-lookup"><span data-stu-id="b5f8b-104">Use Merge Module Registry tables according to the type of registry information.</span></span>

## <a name="typelib-class-appid-progid-extension-verb-or-mime-tables"></a><span data-ttu-id="b5f8b-105">Tablas TypeLib, clase, AppId, ProgId, extensión, verbo o MIME</span><span class="sxs-lookup"><span data-stu-id="b5f8b-105">TypeLib, Class, AppId, ProgId, Extension, Verb, or MIME Tables</span></span>

<span data-ttu-id="b5f8b-106">En el caso de las bibliotecas de tipos, las clases, las extensiones y los verbos, cree información del registro en las tablas [typelib](typelib-table.md), [Class](class-table.md), [AppID](appid-table.md), [ProgID](progid-table.md), [Extension](extension-table.md), [Verb](verb-table.md)o [MIME](mime-table.md) del módulo de combinación.</span><span class="sxs-lookup"><span data-stu-id="b5f8b-106">For type libraries, classes, extensions, and verbs, author registry information into the merge module's [TypeLib](typelib-table.md), [Class](class-table.md), [AppId](appid-table.md), [ProgId](progid-table.md), [Extension](extension-table.md), [Verb](verb-table.md), or [MIME](mime-table.md) tables.</span></span> <span data-ttu-id="b5f8b-107">Si usa la [tabla del registro](registry-table.md) para agregar esta información, Windows 2000 no puede proporcionar anuncios para estos componentes en todo el sistema.</span><span class="sxs-lookup"><span data-stu-id="b5f8b-107">If you use the [Registry table](registry-table.md) to add this information, Windows 2000 cannot provide system-wide advertisement for these components.</span></span>

<span data-ttu-id="b5f8b-108">Los autores del módulo de combinación pueden decidir no registrarse mediante la tabla de clases por los siguientes motivos:</span><span class="sxs-lookup"><span data-stu-id="b5f8b-108">Merge module authors may decide not to register using the Class table for the following reasons:</span></span>

-   <span data-ttu-id="b5f8b-109">Para que la tabla de clases registre la clase, el archivo debe ser la ruta de acceso de su componente.</span><span class="sxs-lookup"><span data-stu-id="b5f8b-109">To be registered by the Class table, the file has to be the KeyPath of its component.</span></span> <span data-ttu-id="b5f8b-110">Esto puede requerir un cambio inaceptable en la organización de los componentes.</span><span class="sxs-lookup"><span data-stu-id="b5f8b-110">This may require an unacceptable change in the organization of components.</span></span>
-   <span data-ttu-id="b5f8b-111">Una llamada COM puede desencadenar un intento de instalación de la reinstalación de una clase anunciada.</span><span class="sxs-lookup"><span data-stu-id="b5f8b-111">A COM call may trigger an installer attempt to reinstall an advertised class.</span></span> <span data-ttu-id="b5f8b-112">Los autores pueden decidir no registrar una clase mediante la tabla de clases con el fin de evitar la activación de una reinstalación cuando el equipo cliente no admite una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="b5f8b-112">Authors may decide not to register a class using the Class table in order to avoid triggering a reinstallation when the client computer does not support a user interface.</span></span>

## <a name="registry-table"></a><span data-ttu-id="b5f8b-113">Tabla del registro</span><span class="sxs-lookup"><span data-stu-id="b5f8b-113">Registry Table</span></span>

<span data-ttu-id="b5f8b-114">Use la tabla del registro para agregar información del registro que no se puede crear en las tablas TypeLib, Class, AppId, ProgId, Extension, Verb o MIME.</span><span class="sxs-lookup"><span data-stu-id="b5f8b-114">Use the Registry table to add registry information that cannot be authored into the TypeLib, Class, AppId, ProgId, Extension, Verb, or MIME tables.</span></span> <span data-ttu-id="b5f8b-115">Windows 2000 no puede proporcionar un anuncio para todo el sistema para los componentes que utilizan la tabla del registro.</span><span class="sxs-lookup"><span data-stu-id="b5f8b-115">Windows 2000 cannot provide system-wide advertisement for components that use the Registry table.</span></span>

<span data-ttu-id="b5f8b-116">Al crear la tabla del registro, consulte las rutas de acceso de archivo con el \[ \# archivo \] o \[ ! \]Formato de archivo en lugar de un nombre de archivo de \[ directorio \] .</span><span class="sxs-lookup"><span data-stu-id="b5f8b-116">When authoring the Registry table, refer to file paths using the \[\#File\] or \[!File\] format rather than as \[Directory\]Filename.</span></span> <span data-ttu-id="b5f8b-117">El último formato no admite la instalación de ejecución desde el origen.</span><span class="sxs-lookup"><span data-stu-id="b5f8b-117">The latter format does not support run-from-source installation.</span></span> <span data-ttu-id="b5f8b-118">El formato anterior también hace que los archivos que faltan y los componentes defectuosos sean más fáciles de detectar.</span><span class="sxs-lookup"><span data-stu-id="b5f8b-118">The former format also makes missing files and faulty components easier to detect.</span></span>

<span data-ttu-id="b5f8b-119">Se necesita atención cuando se usa texto con formato en la columna de clave de la tabla del registro.</span><span class="sxs-lookup"><span data-stu-id="b5f8b-119">Care is needed when using formatted text in the Key column of the Registry table.</span></span> <span data-ttu-id="b5f8b-120">Dado que Windows Installer no reinstala los componentes que ya están instalados, el uso de texto con formato en este campo puede hacer que las claves del registro queden detrás de la eliminación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b5f8b-120">Because Windows Installer does not reinstall components that are already installed, using formatted text in this field may cause registry keys to be left behind on application removal.</span></span>

## <a name="selfreg-table"></a><span data-ttu-id="b5f8b-121">Tabla SelfReg</span><span class="sxs-lookup"><span data-stu-id="b5f8b-121">SelfReg Table</span></span>

<span data-ttu-id="b5f8b-122">No se recomienda usar la tabla SelfReg.</span><span class="sxs-lookup"><span data-stu-id="b5f8b-122">Using the SelfReg table is not recommended.</span></span> <span data-ttu-id="b5f8b-123">Para obtener una lista de razones para no utilizar el registro automático, consulte [tabla SelfReg](selfreg-table.md).</span><span class="sxs-lookup"><span data-stu-id="b5f8b-123">For a list of reasons for not using self-registration, see [SelfReg table](selfreg-table.md).</span></span> <span data-ttu-id="b5f8b-124">En su lugar, debe usar las tablas TypeLib, Class, AppId, ProgId, Extension, Verb y MIME, siempre que sea posible, y la tabla del registro en todos los demás casos.</span><span class="sxs-lookup"><span data-stu-id="b5f8b-124">You should use the TypeLib, Class, AppId, ProgId, Extension, Verb, and MIME tables where possible instead and the Registry table in all other cases.</span></span>

 

 



