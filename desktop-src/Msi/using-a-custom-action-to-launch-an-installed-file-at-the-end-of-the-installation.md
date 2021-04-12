---
description: En el ejemplo siguiente se muestra cómo iniciar un archivo HTML al final de una instalación de.
ms.assetid: 6b082559-bcfa-4098-b072-27ee78092833
title: Usar una acción personalizada para iniciar un archivo instalado al final de la instalación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e5c039d58830ce6a01f76a0946bced474e5091b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277737"
---
# <a name="using-a-custom-action-to-launch-an-installed-file-at-the-end-of-the-installation"></a><span data-ttu-id="86ac3-103">Usar una acción personalizada para iniciar un archivo instalado al final de la instalación</span><span class="sxs-lookup"><span data-stu-id="86ac3-103">Using a Custom Action to Launch an Installed File at the End of the Installation</span></span>

<span data-ttu-id="86ac3-104">En el ejemplo siguiente se muestra cómo iniciar un archivo HTML al final de una instalación de.</span><span class="sxs-lookup"><span data-stu-id="86ac3-104">The following example illustrates how to launch an HTML file at the end of an installation.</span></span> <span data-ttu-id="86ac3-105">El instalador instala el componente que contiene el archivo y, a continuación, publica un evento de control al final de la instalación para ejecutar una acción personalizada que abre el archivo.</span><span class="sxs-lookup"><span data-stu-id="86ac3-105">The Installer installs the component that contains the file, and then publishes a control event at the end of the installation to run a custom action that opens the file.</span></span> <span data-ttu-id="86ac3-106">Este enfoque se puede usar para iniciar un tutorial de ayuda al final de la primera instalación de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="86ac3-106">This approach may be used to launch a help tutorial at the end of the first installation of an application.</span></span>

<span data-ttu-id="86ac3-107">El ejemplo debe cumplir las siguientes especificaciones.</span><span class="sxs-lookup"><span data-stu-id="86ac3-107">The sample must meet the following specifications.</span></span>

-   <span data-ttu-id="86ac3-108">El instalador ejecuta la acción personalizada solo si se usa el nivel de [*interfaz de usuario completo*](f-gly.md) para instalar una aplicación.</span><span class="sxs-lookup"><span data-stu-id="86ac3-108">The Installer executes the custom action only if the [*full UI*](f-gly.md) level is used to install an application.</span></span>
-   <span data-ttu-id="86ac3-109">El instalador ejecuta la acción personalizada solo si el componente que contiene el archivo HTML está instalado para ejecutarse localmente en el equipo.</span><span class="sxs-lookup"><span data-stu-id="86ac3-109">The Installer executes the custom action only if the component that contains the HTML file is installed to run locally on the computer.</span></span>
-   <span data-ttu-id="86ac3-110">La acción personalizada solo se ejecuta en la primera instalación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="86ac3-110">The custom action only runs on the first installation of the application.</span></span>
-   <span data-ttu-id="86ac3-111">No se produce un error en la instalación si se produce un error en la acción personalizada.</span><span class="sxs-lookup"><span data-stu-id="86ac3-111">The installation does not fail if the custom action fails.</span></span>

<span data-ttu-id="86ac3-112">El ejemplo incluye un componente hipotético denominado tutorial que controla al menos un recurso, un archivo denominado tutorial.htm.</span><span class="sxs-lookup"><span data-stu-id="86ac3-112">The sample includes a hypothetical component named Tutorial that controls at least one resource, a file named tutorial.htm.</span></span> <span data-ttu-id="86ac3-113">El identificador de este archivo en la columna de archivo de la tabla de archivos es tutorial.</span><span class="sxs-lookup"><span data-stu-id="86ac3-113">The identifier for this file in the File column of the File table is Tutorial.</span></span> <span data-ttu-id="86ac3-114">En el siguiente debate se supone que ya ha creado los recursos necesarios para el tutorial y que han realizado todas las entradas necesarias en las tablas de [características](feature-table.md), [componentes](component-table.md), [archivos](file-table.md), [directorios](directory-table.md)y [FeatureComponents](featurecomponents-table.md) para instalar este componente.</span><span class="sxs-lookup"><span data-stu-id="86ac3-114">The following discussion assumes that you have already created the resources required by Tutorial, and have made all the necessary entries in the [Feature](feature-table.md), [Component](component-table.md), [File](file-table.md), [Directory](directory-table.md), and [FeatureComponents](featurecomponents-table.md) tables to install this component.</span></span> <span data-ttu-id="86ac3-115">Para obtener más información, vea [un ejemplo de instalación](an-installation-example.md).</span><span class="sxs-lookup"><span data-stu-id="86ac3-115">For more information, see [An Installation Example](an-installation-example.md).</span></span>

<span data-ttu-id="86ac3-116">Los temas siguientes contienen información acerca de cómo crear las acciones personalizadas necesarias y agregarlas a un paquete de instalación.</span><span class="sxs-lookup"><span data-stu-id="86ac3-116">The following topics contain information about how to create required custom actions and add them to an installation package.</span></span>

-   [<span data-ttu-id="86ac3-117">Crear la acción personalizada iniciar</span><span class="sxs-lookup"><span data-stu-id="86ac3-117">Authoring the Launch Custom Action</span></span>](authoring-the-launch-custom-action.md)
-   [<span data-ttu-id="86ac3-118">Adición del inicio a las tablas de CustomAction y binarias</span><span class="sxs-lookup"><span data-stu-id="86ac3-118">Adding Launch to the CustomAction and Binary Tables</span></span>](adding-launch-to-the-customaction-and-binary-tables.md)
-   [<span data-ttu-id="86ac3-119">Agregar un evento de control al final de la instalación para ejecutar el inicio</span><span class="sxs-lookup"><span data-stu-id="86ac3-119">Adding a Control Event at the End of the Installation to Run Launch</span></span>](adding-a-control-event-at-the-end-of-the-installation-to-run-launch.md)

 

 



