---
description: Los predicados de profundidad de carpeta controlan el ámbito de una búsqueda especificando una ruta de acceso y si se realiza un recorrido profundo o superficial.
ms.assetid: 8eadbd42-3538-412e-9bf8-b2355d23437e
title: Predicados de ámbito y directorio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2418b2149a5bf05bd000460c787b7f967856c5c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153961"
---
# <a name="scope-and-directory-predicates"></a><span data-ttu-id="8a678-103">Predicados de ámbito y directorio</span><span class="sxs-lookup"><span data-stu-id="8a678-103">SCOPE and DIRECTORY Predicates</span></span>

<span data-ttu-id="8a678-104">Los predicados de profundidad de carpeta controlan el ámbito de una búsqueda especificando una ruta de acceso y si se realiza un recorrido profundo o superficial.</span><span class="sxs-lookup"><span data-stu-id="8a678-104">Folder depth predicates control the scope of a search by specifying a path and whether to perform a deep or shallow traversal.</span></span> <span data-ttu-id="8a678-105">A continuación se muestra la sintaxis de los predicados de profundidad de la carpeta:</span><span class="sxs-lookup"><span data-stu-id="8a678-105">The following shows the syntax of the folder depth predicates:</span></span>


```
... WHERE [{SCOPE | DIRECTORY}='<protocol>:[{SID}]<path>']
```



<span data-ttu-id="8a678-106">El predicado va seguido de un signo igual.</span><span class="sxs-lookup"><span data-stu-id="8a678-106">The predicate is followed by an equal sign.</span></span> <span data-ttu-id="8a678-107">La ruta de acceso se incluye entre comillas simples y debe comenzar por un protocolo y dos puntos (por ejemplo, `file:` , `mapi:` o `csc:` ).</span><span class="sxs-lookup"><span data-stu-id="8a678-107">The path is exclosed in single quotes and must begin with a protocol and a colon (for example, `file:`, `mapi:`, or `csc:`).</span></span> <span data-ttu-id="8a678-108">El predicado de ámbito realiza un recorrido profundo de la ruta de acceso, incluidas todas las subcarpetas, mientras que el predicado de directorio realiza un recorrido superficial solo de la carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="8a678-108">The SCOPE predicate performs a deep traversal of the path, including all subfolders, while the DIRECTORY predicate does a shallow traversal of only the folder specified.</span></span> <span data-ttu-id="8a678-109">Al igual que otras restricciones de Lenguaje de consulta estructurado (SQL), puede especificar más de una restricción de profundidad de carpeta en una sola consulta.</span><span class="sxs-lookup"><span data-stu-id="8a678-109">Like other Structured Query Language (SQL) restrictions, you can specify more than one folder depth restriction in a single query.</span></span>

<span data-ttu-id="8a678-110">Para consultar el catálogo local de un equipo remoto, incluya el nombre del equipo delante del catálogo y una ruta de acceso UNC (Convención de nomenclatura universal) en el equipo remoto en la cláusula SCOPE o DIRECTORY.</span><span class="sxs-lookup"><span data-stu-id="8a678-110">To query the local catalog of a remote computer, include the computer name before the catalog and a Universal Naming Convention (UNC) path on the remote computer in the SCOPE or DIRECTORY clause.</span></span>

## <a name="examples"></a><span data-ttu-id="8a678-111">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8a678-111">Examples</span></span>


```
SELECT System.ItemName FROM SystemIndex WHERE SCOPE='file:C:/Files/Reports'

SELECT System.ItemName FROM SystemIndex WHERE DIRECTORY='file:C:/Files/Reports' 

SELECT System.ItemName FROM SystemIndex WHERE SCOPE='file:C:/Files/Published' OR SCOPE='file:C:/Files/Reports' AND NOT SCOPE='file:C:/Files/Reports/Confidential'

SELECT System.ItemName FROM zarasmachine.SystemIndex WHERE SCOPE='file://zarasmachine/C:/Files/Reports'

SELECT System.ItemURL FROM SystemIndex WHERE SCOPE='mapi://{S-1-5-21-2117521111-1604012920-1887927527-2285604}/Mailbox user/' AND CONTAINS('Microsoft')
```



<span data-ttu-id="8a678-112">En el primer ejemplo de ámbito se busca en la carpeta C: \\ files \\ Reports y en todas sus subcarpetas.</span><span class="sxs-lookup"><span data-stu-id="8a678-112">The first SCOPE example searches the C:\\Files\\Reports folder and all its subfolders.</span></span> <span data-ttu-id="8a678-113">En el ejemplo de directorio solo se buscan en la carpeta raíz los informes C: \\ archivos \\ .</span><span class="sxs-lookup"><span data-stu-id="8a678-113">The DIRECTORY example searches only the root folder C:\\Files\\Reports.</span></span>

> [!Note]  
> <span data-ttu-id="8a678-114">Las barras diagonales inversas del sistema de archivos ( \\ ) se convierten en una barra diagonal de estilo URL (a veces llamadas barras diagonales) (/).</span><span class="sxs-lookup"><span data-stu-id="8a678-114">The file system backslashes (\\) become a URL-style slash marks (sometimes called forward slashes) (/).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="8a678-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8a678-115">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="8a678-116">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="8a678-116">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8a678-117">Cláusula FROM</span><span class="sxs-lookup"><span data-stu-id="8a678-117">FROM Clause</span></span>](-search-sql-from.md)
</dt> <dt>

[<span data-ttu-id="8a678-118">Cláusula WHERE</span><span class="sxs-lookup"><span data-stu-id="8a678-118">WHERE Clause</span></span>](-search-sql-where.md)
</dt> </dl>

 

 



