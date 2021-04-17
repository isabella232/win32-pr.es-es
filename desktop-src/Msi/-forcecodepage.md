---
description: La \_ tabla ForceCodepage es una tabla especial que se usa para cambiar la página de códigos de un paquete de instalación. Puede determinar o establecer la página de códigos exportando o importando un archivo de almacenamiento de texto denominado \_ ForceCodepage. IDT.
ms.assetid: d95c205f-a800-4a63-a712-6f06675e4a8a
title: _ForceCodepage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 132843fa092409b26811afd6a4c1f3e7cf0544f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667082"
---
# <a name="_forcecodepage"></a><span data-ttu-id="45d64-104">\_ForceCodepage</span><span class="sxs-lookup"><span data-stu-id="45d64-104">\_ForceCodepage</span></span>

<span data-ttu-id="45d64-105">La \_ tabla ForceCodepage es una tabla especial que se usa para cambiar la página de códigos de un paquete de instalación.</span><span class="sxs-lookup"><span data-stu-id="45d64-105">The \_ForceCodepage table is a special table used for changing the code page of an installation package.</span></span> <span data-ttu-id="45d64-106">Puede determinar o establecer la página de códigos exportando o importando un [archivo de almacenamiento de texto](text-archive-files.md) denominado \_ ForceCodepage. IDT.</span><span class="sxs-lookup"><span data-stu-id="45d64-106">You can determine or set the code page by exporting or importing a [text archive file](text-archive-files.md) named \_ForceCodepage.idt.</span></span>

<span data-ttu-id="45d64-107">El formato de la \_ tabla ForceCodepage es 2 líneas en blanco seguidas de una tercera línea que indica la página de códigos numérica.</span><span class="sxs-lookup"><span data-stu-id="45d64-107">The format of the \_ForceCodepage table is 2 blank lines followed by a third line that indicates the numeric code page.</span></span> <span data-ttu-id="45d64-108">Por ejemplo, un \_ archivo Table. IDT de ForceCodepage para una base de datos japonesa tendría el siguiente aspecto.</span><span class="sxs-lookup"><span data-stu-id="45d64-108">For example, a \_ForceCodepage table .idt file for a Japanese database would look as follows.</span></span> <span data-ttu-id="45d64-109">En este caso, la página de códigos numérica es 932.</span><span class="sxs-lookup"><span data-stu-id="45d64-109">The numeric code page in this case is 932.</span></span>

``` syntax
<- this line blank
<- this line blank
932 _ForceCodepage
```

<span data-ttu-id="45d64-110">Para obtener más información sobre cómo usar \_ ForceCodepage para obtener o establecer la página de códigos de una base de datos, vea los temas siguientes.</span><span class="sxs-lookup"><span data-stu-id="45d64-110">For more information on how to use \_ForceCodepage to get or set the code page of a database see the following topics.</span></span>

-   [<span data-ttu-id="45d64-111">Control de páginas de códigos (Windows Installer)</span><span class="sxs-lookup"><span data-stu-id="45d64-111">Code Page Handling (Windows Installer)</span></span>](code-page-handling-windows-installer-.md)
-   [<span data-ttu-id="45d64-112">Determinar la página de códigos de una base de datos de instalación</span><span class="sxs-lookup"><span data-stu-id="45d64-112">Determining an Installation Database's Code Page</span></span>](determining-an-installation-database-s-code-page.md)
-   [<span data-ttu-id="45d64-113">Establecer la página de códigos de una base de datos</span><span class="sxs-lookup"><span data-stu-id="45d64-113">Setting the Code Page of a Database</span></span>](setting-the-code-page-of-a-database.md)

<span data-ttu-id="45d64-114">La \_ tabla ForceCodepage es una pseudo tabla especial que se usa para cambiar la página de códigos de un paquete de instalación.</span><span class="sxs-lookup"><span data-stu-id="45d64-114">The \_ForceCodepage table is a special pseudo table used for changing the code page of an installation package.</span></span> <span data-ttu-id="45d64-115">El uso de la \_ tabla ForceCodepage establece incondicionalmente la base de datos en la página de códigos sin realizar ninguna validación en cuanto a si los datos que se encuentran actualmente en la base de datos se pueden traducir en la nueva página de códigos.</span><span class="sxs-lookup"><span data-stu-id="45d64-115">Using the \_ForceCodepage table unconditionally sets the database to the code page without performing any validation as to whether the data currently in the database can be translated to the new code page.</span></span> <span data-ttu-id="45d64-116">Siempre se recomienda que el cambio de la página de códigos de una base de datos comience con una base de datos independiente del lenguaje.</span><span class="sxs-lookup"><span data-stu-id="45d64-116">It is always recommended that changing the code page of a database start with a language neutral database.</span></span>

 

 



