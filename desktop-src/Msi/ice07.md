---
description: ICE07 valida que el paquete de instalación especifica que las fuentes se instalan en FontsFolder. Si una fuente se instala en una carpeta que no sea la FontsFolder, el instalador crea un acceso directo en lugar de instalar realmente la fuente.
ms.assetid: aa51b077-fb7b-4e09-9de1-ef1905144a94
title: ICE07
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80a79bcb681a57bb09ff235b35a5287492a4f39c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652821"
---
# <a name="ice07"></a><span data-ttu-id="5d772-104">ICE07</span><span class="sxs-lookup"><span data-stu-id="5d772-104">ICE07</span></span>

<span data-ttu-id="5d772-105">ICE07 valida que el paquete de instalación especifica que las fuentes se instalan en FontsFolder.</span><span class="sxs-lookup"><span data-stu-id="5d772-105">ICE07 validates that installation package specifies that fonts be installed into the FontsFolder.</span></span> <span data-ttu-id="5d772-106">Si una fuente se instala en una carpeta que no sea la FontsFolder, el instalador crea un acceso directo en lugar de instalar realmente la fuente.</span><span class="sxs-lookup"><span data-stu-id="5d772-106">If a font is installed to a folder other than the FontsFolder the installer creates a shortcut rather than actually installing the font.</span></span>

<span data-ttu-id="5d772-107">La acción personalizada ICE07 realiza lo siguiente para cada fuente de la [tabla de fuentes](font-table.md).</span><span class="sxs-lookup"><span data-stu-id="5d772-107">The ICE07 custom action does the following for each font in the [Font table](font-table.md).</span></span>

1.  <span data-ttu-id="5d772-108">Busca el archivo de fuente al que pertenece cada título de fuente mediante la [tabla de fuentes](font-table.md).</span><span class="sxs-lookup"><span data-stu-id="5d772-108">Finds the font file to which each font title belongs using the [Font table](font-table.md).</span></span>
2.  <span data-ttu-id="5d772-109">Consulta la \_ columna componente de la [tabla de archivos](file-table.md) del componente que controla cada archivo.</span><span class="sxs-lookup"><span data-stu-id="5d772-109">Queries the Component\_ column of the [File table](file-table.md) for the component that controls each file.</span></span>
3.  <span data-ttu-id="5d772-110">Consulta la \_ columna directorio de la [tabla de componentes](component-table.md) para obtener una clave en la tabla de directorios.</span><span class="sxs-lookup"><span data-stu-id="5d772-110">Queries the Directory\_ column of the [Component table](component-table.md) to obtain a key into the Directory table.</span></span>
4.  <span data-ttu-id="5d772-111">Resuelve la tabla de [directorio](directory-table.md) para determinar el nombre de la carpeta en la que el instalador va a instalar el archivo de fuente.</span><span class="sxs-lookup"><span data-stu-id="5d772-111">Resolves the [Directory table](directory-table.md) to determine the name of the folder into which the installer is to install the font file</span></span>
5.  <span data-ttu-id="5d772-112">Envía un error si el archivo de fuente se instala en una carpeta distinta de FontsFolder.</span><span class="sxs-lookup"><span data-stu-id="5d772-112">Posts an error if the font file is being installed into a folder other than the FontsFolder.</span></span>

## <a name="result"></a><span data-ttu-id="5d772-113">Resultado</span><span class="sxs-lookup"><span data-stu-id="5d772-113">Result</span></span>

<span data-ttu-id="5d772-114">ICE07 publica un error si detecta que la base de datos especifica que un archivo de fuente se instala en una carpeta distinta de la FontsFolder.</span><span class="sxs-lookup"><span data-stu-id="5d772-114">ICE07 posts an error if it finds that the database specifies that a font file be installed into a folder other than the FontsFolder.</span></span>

## <a name="example"></a><span data-ttu-id="5d772-115">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5d772-115">Example</span></span>

<span data-ttu-id="5d772-116">IC07 publicaría el mensaje de error siguiente para el ejemplo mostrado.</span><span class="sxs-lookup"><span data-stu-id="5d772-116">IC07 would post the following error message for the example shown.</span></span>

``` syntax
'Tahoma' is a font and must be installed to the FontsFolder directory. Current Install Directory: 'Sandbar'.
```

[<span data-ttu-id="5d772-117">Tabla de fuentes</span><span class="sxs-lookup"><span data-stu-id="5d772-117">Font Table</span></span>](font-table.md)



| <span data-ttu-id="5d772-118">Archivo\_</span><span class="sxs-lookup"><span data-stu-id="5d772-118">File\_</span></span> | <span data-ttu-id="5d772-119">FontTitle</span><span class="sxs-lookup"><span data-stu-id="5d772-119">FontTitle</span></span> |
|--------|-----------|
| <span data-ttu-id="5d772-120">Myrtle</span><span class="sxs-lookup"><span data-stu-id="5d772-120">Myrtle</span></span> | <span data-ttu-id="5d772-121">Tahoma</span><span class="sxs-lookup"><span data-stu-id="5d772-121">Tahoma</span></span>    |



 

<span data-ttu-id="5d772-122">[Tabla de archivos](file-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="5d772-122">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="5d772-123">Archivo</span><span class="sxs-lookup"><span data-stu-id="5d772-123">File</span></span>   | <span data-ttu-id="5d772-124">Componente\_</span><span class="sxs-lookup"><span data-stu-id="5d772-124">Component\_</span></span>   |
|--------|---------------|
| <span data-ttu-id="5d772-125">Myrtle</span><span class="sxs-lookup"><span data-stu-id="5d772-125">Myrtle</span></span> | <span data-ttu-id="5d772-126">Myrtle \_ Beach</span><span class="sxs-lookup"><span data-stu-id="5d772-126">Myrtle\_Beach</span></span> |



 

<span data-ttu-id="5d772-127">[Tabla de componentes](component-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="5d772-127">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="5d772-128">Componente</span><span class="sxs-lookup"><span data-stu-id="5d772-128">Component</span></span>     | <span data-ttu-id="5d772-129">Directorio\_</span><span class="sxs-lookup"><span data-stu-id="5d772-129">Directory\_</span></span> |
|---------------|-------------|
| <span data-ttu-id="5d772-130">Myrtle \_ Beach</span><span class="sxs-lookup"><span data-stu-id="5d772-130">Myrtle\_Beach</span></span> | <span data-ttu-id="5d772-131">SandBar</span><span class="sxs-lookup"><span data-stu-id="5d772-131">SandBar</span></span>     |



 

<span data-ttu-id="5d772-132">En este ejemplo, la fuente Tahoma se asigna al archivo de fuente Myrtle.</span><span class="sxs-lookup"><span data-stu-id="5d772-132">In this example, the font Tahoma maps to the font file Myrtle.</span></span> <span data-ttu-id="5d772-133">El archivo Myrtle pertenece al componente Myrtle \_ Beach.</span><span class="sxs-lookup"><span data-stu-id="5d772-133">The file Myrtle belongs to the component Myrtle\_Beach.</span></span> <span data-ttu-id="5d772-134">La resolución de la tabla de directorios muestra que todos los archivos que pertenecen a Myrtle \_ Beach se van a instalar en la carpeta Sandbar.</span><span class="sxs-lookup"><span data-stu-id="5d772-134">Resolution of the Directory table shows that all the files belonging to Myrtle\_Beach are to be installed in the Sandbar folder.</span></span> <span data-ttu-id="5d772-135">Como no se FontsFolder, ICE07 envía un mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="5d772-135">Because this is not the FontsFolder, ICE07 posts an error message.</span></span>

<span data-ttu-id="5d772-136">Tenga en cuenta que si el componente Myrtle \_ Beach realmente pertenece a la carpeta Sandbar, y no al FontsFolder, es posible que la fuente Tahoma no pertenezca a Myrtle \_ Beach.</span><span class="sxs-lookup"><span data-stu-id="5d772-136">Note that if the component Myrtle\_Beach really belongs in the Sandbar folder, and not the FontsFolder, then the font Tahoma may not belong in Myrtle\_Beach.</span></span> <span data-ttu-id="5d772-137">Una posible solución para el error sería incluir Tahoma en otro componente que se instala en el directorio FontsFolder</span><span class="sxs-lookup"><span data-stu-id="5d772-137">A possible fix for the error would be to include Tahoma in another component that does get installed in the FontsFolder directory.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5d772-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5d772-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d772-139">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="5d772-139">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



