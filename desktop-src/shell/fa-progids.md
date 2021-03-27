---
description: El shell utiliza una subclave del registro de identificador de programación (ProgID) para asociar un tipo de archivo a una aplicación y controlar el comportamiento de la asociación.
ms.assetid: f2b666d6-bf22-47b5-87e1-8de5ff51c152
title: Identificadores de programación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67720fed1ad4b8401d11f6532cdc79836911e7cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997221"
---
# <a name="programmatic-identifiers"></a><span data-ttu-id="6790b-103">Identificadores de programación</span><span class="sxs-lookup"><span data-stu-id="6790b-103">Programmatic Identifiers</span></span>

<span data-ttu-id="6790b-104">El shell utiliza una subclave del registro de identificador de programación (ProgID) para asociar un tipo de archivo a una aplicación y controlar el comportamiento de la asociación.</span><span class="sxs-lookup"><span data-stu-id="6790b-104">The Shell uses a programmatic identifier (ProgID) registry subkey to associate a file type with an application, and to control the behavior of the association.</span></span> <span data-ttu-id="6790b-105">Las entradas ProgID utilizadas para las asociaciones de archivo se encuentran en **HKEY \_ classes \_ root** en el registro.</span><span class="sxs-lookup"><span data-stu-id="6790b-105">The ProgID entries used for file associations are located under **HKEY\_CLASSES\_ROOT** in the registry.</span></span>

<span data-ttu-id="6790b-106">Este tema se organiza de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="6790b-106">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="6790b-107">Elementos de identificador de programación usados por las asociaciones de archivo</span><span class="sxs-lookup"><span data-stu-id="6790b-107">Programmatic Identifier Elements Used by File Associations</span></span>](#programmatic-identifier-elements-used-by-file-associations)
-   [<span data-ttu-id="6790b-108">Usar identificadores de programación con versión</span><span class="sxs-lookup"><span data-stu-id="6790b-108">Using Versioned Programmatic Identifiers</span></span>](#using-versioned-programmatic-identifiers)
-   [<span data-ttu-id="6790b-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6790b-109">Related topics</span></span>](#related-topics)

<span data-ttu-id="6790b-110">Para obtener más información, consulte [registro de un tipo de archivo para una nueva aplicación](how-to-register-a-file-type-for-a-new-application.md) .</span><span class="sxs-lookup"><span data-stu-id="6790b-110">For additional information, read [How To Register a File Type for a New Application](how-to-register-a-file-type-for-a-new-application.md)</span></span>

## <a name="programmatic-identifier-elements-used-by-file-associations"></a><span data-ttu-id="6790b-111">Elementos de identificador de programación usados por las asociaciones de archivo</span><span class="sxs-lookup"><span data-stu-id="6790b-111">Programmatic Identifier Elements Used by File Associations</span></span>

<span data-ttu-id="6790b-112">El formato correcto de un nombre de clave ProgID es \[ *Vendor o Application* \] . \[ *Componente* \] . \[ *Versión* \] , separados por puntos y sin espacios, como en Word.Document. 6.</span><span class="sxs-lookup"><span data-stu-id="6790b-112">The proper format of a ProgID key name is \[*Vendor or Application*\].\[*Component*\].\[*Version*\], separated by periods and with no spaces, as in Word.Document.6.</span></span> <span data-ttu-id="6790b-113">La parte de la *versión* es opcional, pero se recomienda encarecidamente.</span><span class="sxs-lookup"><span data-stu-id="6790b-113">The *Version* portion is optional but strongly recommended.</span></span> <span data-ttu-id="6790b-114">Para obtener más información, vea [usar identificadores de programación con versiones](#using-versioned-programmatic-identifiers).</span><span class="sxs-lookup"><span data-stu-id="6790b-114">For more information, see [Using Versioned Programmatic Identifiers](#using-versioned-programmatic-identifiers).</span></span>

<span data-ttu-id="6790b-115">Una subclave ProgID debe incluir los elementos siguientes.</span><span class="sxs-lookup"><span data-stu-id="6790b-115">A ProgID subkey should include the following elements.</span></span> <span data-ttu-id="6790b-116">Tenga en cuenta que algunos datos de cadena de esta clave requieren un formato específico.</span><span class="sxs-lookup"><span data-stu-id="6790b-116">Note that some string data in this key requires specific formatting.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6790b-117">Elemento</span><span class="sxs-lookup"><span data-stu-id="6790b-117">Element</span></span></th>
<th><span data-ttu-id="6790b-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="6790b-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6790b-119"><strong>Predeterminada</strong></span><span class="sxs-lookup"><span data-stu-id="6790b-119"><strong>(Default)</strong></span></span></td>
<td><span data-ttu-id="6790b-120">Establezca la entrada predeterminada de la subclave ProgID en un nombre descriptivo para ese ProgID, que se pueda mostrar al usuario.</span><span class="sxs-lookup"><span data-stu-id="6790b-120">Set the default entry of the ProgID subkey to a friendly name for that ProgID, suitable to display to the user.</span></span> <span data-ttu-id="6790b-121">El uso de esta entrada para contener el nombre descriptivo está en desuso en la entrada FriendlyTypeName en sistemas que ejecutan Windows 2000 o posterior.</span><span class="sxs-lookup"><span data-stu-id="6790b-121">The use of this entry to hold the friendly name is deprecated by the FriendlyTypeName entry on systems running Windows 2000 or later.</span></span> <span data-ttu-id="6790b-122">Sin embargo, debe establecer este valor para mantener la compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="6790b-122">However, you should set this value for backward compatibility.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6790b-123"><strong>AllowSilentDefaultTakeOver</strong> (introducido en Windows 8)</span><span class="sxs-lookup"><span data-stu-id="6790b-123"><strong>AllowSilentDefaultTakeOver</strong> (introduced in Windows 8)</span></span></td>
<td><span data-ttu-id="6790b-124">Establezca esta entrada opcional para indicar que Windows debe omitir este ProgID al determinar un controlador predeterminado para un tipo de archivo público.</span><span class="sxs-lookup"><span data-stu-id="6790b-124">Set this optional entry to signal that Windows should ignore this ProgID when determining a default handler for a public file type.</span></span> <span data-ttu-id="6790b-125">Independientemente de si se establece este valor, el ProgID seguirá apareciendo en el cuadro de diálogo y el menú contextual de OpenWith.</span><span class="sxs-lookup"><span data-stu-id="6790b-125">Regardless of whether this value is set, the ProgID continues to appear in the OpenWith shortcut menu and dialog.</span></span> <span data-ttu-id="6790b-126">Se trata de un valor de REG_NONE.</span><span class="sxs-lookup"><span data-stu-id="6790b-126">This is a REG_NONE value.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6790b-127"><strong>AppUserModelID</strong> (introducido en Windows 7)</span><span class="sxs-lookup"><span data-stu-id="6790b-127"><strong>AppUserModelID</strong> (introduced in Windows 7)</span></span></td>
<td><span data-ttu-id="6790b-128">Establezca esta entrada opcional en el identificador de modelo de usuario de la aplicación explícito de la aplicación (AppUserModelID) si la aplicación usa un AppUserModelID explícito y usa las listas de acceso <strong>frecuente</strong> o <strong>recientes</strong> generadas automáticamente del sistema, o proporciona una Jump List personalizada.</span><span class="sxs-lookup"><span data-stu-id="6790b-128">Set this optional entry to the application's explicit Application User Model ID (AppUserModelID) if the application uses an explicit AppUserModelID and uses either the system's automatically generated <strong>Recent</strong> or <strong>Frequent</strong> Jump Lists or provides a custom Jump List.</span></span> <span data-ttu-id="6790b-129">Si una aplicación utiliza un AppUserModelID explícito y no establece este valor, los elementos no aparecerán en las Jump Lists de esa aplicación.</span><span class="sxs-lookup"><span data-stu-id="6790b-129">If an application uses an explicit AppUserModelID and does not set this value, items will not appear in that application's Jump Lists.</span></span> <span data-ttu-id="6790b-130">Se trata de una cadena de REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="6790b-130">This is a REG_SZ string.</span></span> <span data-ttu-id="6790b-131">Para obtener más información, vea <a href="appids.md">identificadores de modelo de usuario de la aplicación (AppUserModelIDs)</a>.</span><span class="sxs-lookup"><span data-stu-id="6790b-131">For more information, see <a href="appids.md">Application User Model IDs (AppUserModelIDs)</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6790b-132"><strong>EditFlags</strong></span><span class="sxs-lookup"><span data-stu-id="6790b-132"><strong>EditFlags</strong></span></span></td>
<td><span data-ttu-id="6790b-133">Establezca esta entrada opcional mediante marcas de la enumeración <a href="/windows/desktop/api/Shlwapi/ne-shlwapi-filetypeattributeflags"><strong>FILETYPEATTRIBUTEFLAGS</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="6790b-133">Set this optional entry using flags from the <a href="/windows/desktop/api/Shlwapi/ne-shlwapi-filetypeattributeflags"><strong>FILETYPEATTRIBUTEFLAGS</strong></a> enumeration.</span></span> <span data-ttu-id="6790b-134">La entrada marcas controla algunos aspectos de la administración del shell de los tipos de archivo vinculados a este ProgID.</span><span class="sxs-lookup"><span data-stu-id="6790b-134">The EditFlags entry controls some aspects of the Shell's handling of the file types linked to this ProgID.</span></span> <span data-ttu-id="6790b-135">También puede usar la entrada marcas para limitar la cantidad de tiempo que el usuario puede modificar determinados aspectos de estos tipos de archivo mediante la hoja de propiedades de un archivo.</span><span class="sxs-lookup"><span data-stu-id="6790b-135">You can also use the EditFlags entry to limit how much the user can modify certain aspects of these file types using a file's property sheet.</span></span> <span data-ttu-id="6790b-136">Los valores de <strong>FILETYPEATTRIBUTEFLAGS</strong> usados para marcas son valores binarios diseñados para que pueda combinar varios atributos en un solo valor en una operación OR bit a bit.</span><span class="sxs-lookup"><span data-stu-id="6790b-136">The <strong>FILETYPEATTRIBUTEFLAGS</strong> values used for EditFlags are binary values designed so that you can combine multiple attributes into a single value in a bitwise OR operation.</span></span> <span data-ttu-id="6790b-137">Se trata de un valor REG_DWORD o REG_BINARY.</span><span class="sxs-lookup"><span data-stu-id="6790b-137">This is a REG_DWORD or REG_BINARY value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6790b-138"><strong>FriendlyTypeName</strong></span><span class="sxs-lookup"><span data-stu-id="6790b-138"><strong>FriendlyTypeName</strong></span></span></td>
<td><span data-ttu-id="6790b-139">Establezca esta entrada en un nombre descriptivo para el ProgID, que se pueda mostrar al usuario.</span><span class="sxs-lookup"><span data-stu-id="6790b-139">Set this entry to a friendly name for the ProgID, suitable to display to the user.</span></span> <span data-ttu-id="6790b-140">Por coherencia, esta cadena debe contener los mismos datos que la entrada predeterminada para esta clave ProgID.</span><span class="sxs-lookup"><span data-stu-id="6790b-140">For consistency, this string should contain the same data as the Default entry for this ProgID key.</span></span> <span data-ttu-id="6790b-141">Esta entrada puede ser una cadena REG_SZ o REG_EXPAND_SZ, pero debe tener el formato de una cadena indirecta (un nombre de archivo completo y un valor de recurso precedidos del símbolo @), por ejemplo, <em>@% systemroot% \shell32.dll,-154</em>.</span><span class="sxs-lookup"><span data-stu-id="6790b-141">This entry can be either a REG_SZ or REG_EXPAND_SZ string, but it must be formatted as an indirect string (a fully qualified file name and resource value preceded by the @ symbol), for instance <em>@%SystemRoot%\shell32.dll,-154</em>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6790b-142"><strong>InfoTip</strong></span><span class="sxs-lookup"><span data-stu-id="6790b-142"><strong>InfoTip</strong></span></span></td>
<td><span data-ttu-id="6790b-143">Establezca esta entrada en un breve mensaje de ayuda que el shell muestre para este ProgID.</span><span class="sxs-lookup"><span data-stu-id="6790b-143">Set this entry to a brief help message that the Shell displays for this ProgID.</span></span> <span data-ttu-id="6790b-144">La entrada de recuadro informativo se muestra en un cuadro de diálogo de pasar el mouse.</span><span class="sxs-lookup"><span data-stu-id="6790b-144">The InfoTip entry displays in a mouse-over dialog box.</span></span> <span data-ttu-id="6790b-145">Este valor puede ser una cadena REG_SZ o REG_EXPAND_SZ pero, como FriendlyTypeName, debe tener el formato de una cadena indirecta.</span><span class="sxs-lookup"><span data-stu-id="6790b-145">This value can be either a REG_SZ or REG_EXPAND_SZ string but, like FriendlyTypeName, it must be formatted as an indirect string.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6790b-146"><strong>CurVer</strong></span><span class="sxs-lookup"><span data-stu-id="6790b-146"><strong>CurVer</strong></span></span></td>
<td><span data-ttu-id="6790b-147">Establezca la entrada (predeterminada) de esta subclave en la versión más reciente de este ProgID.</span><span class="sxs-lookup"><span data-stu-id="6790b-147">Set the (Default) entry of this subkey to the most current version of this ProgID.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="6790b-148">A menos que tenga versiones de aplicaciones en paralelo, es decir, varias versiones instaladas en el mismo sistema, debe evitar el uso de <strong>curver</strong>.</span><span class="sxs-lookup"><span data-stu-id="6790b-148">Unless you have side-by-side application versions, that is, multiple versions installed on the same system, you should avoid using <strong>CurVer</strong>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6790b-149"><strong>DefaultIcon</strong>.</span><span class="sxs-lookup"><span data-stu-id="6790b-149"><strong>DefaultIcon</strong>.</span></span></td>
<td><span data-ttu-id="6790b-150">Establezca la entrada (predeterminada) de esta subclave en el icono predeterminado que desea mostrar para los tipos de archivo asociados a este ProgID.</span><span class="sxs-lookup"><span data-stu-id="6790b-150">Set the (Default) entry of this subkey to the default icon that you want to display for file types associated with this ProgID.</span></span> <span data-ttu-id="6790b-151">Este valor puede ser un REG_SZ o REG_EXPAND_SZ cadena, pero se debe proporcionar como un nombre de archivo completo con su valor de recurso de operador, por ejemplo, <em>% systemroot% \shell32.dll,-154</em>.</span><span class="sxs-lookup"><span data-stu-id="6790b-151">This value can be either a REG_SZ or REG_EXPAND_SZ string, but it must be provided as a fully qualified file name with its attendant resource value, for instance <em>%SystemRoot%\shell32.dll,-154</em>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="6790b-152">El siguiente ejemplo de clave del registro ilustra un nodo de clave ProgID de Asociación de archivo:</span><span class="sxs-lookup"><span data-stu-id="6790b-152">The following registry key example illustrates a file association ProgID key node:</span></span>

```
HKEY_CLASSES_ROOT
   Vendor.App.1
      (Default) = My Friendly Name
      AllowSilentDefaultTakeOver
      AppUserModelID = Vendor.Application
      EditFlags = 0x00000001
      FriendlyTypeName = @%SystemRoot%\shell32.dll,-154
      InfoTip = @%SystemRoot%\shell32.dll,-54
      CurVer
         (Default) = Vendor.App.1
      DefaultIcon
         (Default) = %SystemRoot%\shell32.dll,-1
```

## <a name="using-versioned-programmatic-identifiers"></a><span data-ttu-id="6790b-153">Usar identificadores de programación con versión</span><span class="sxs-lookup"><span data-stu-id="6790b-153">Using Versioned Programmatic Identifiers</span></span>

<span data-ttu-id="6790b-154">Un ProgID con versión es aquél cuya versión se indica en su nombre.</span><span class="sxs-lookup"><span data-stu-id="6790b-154">A versioned ProgID is one whose version is indicated in its name.</span></span> <span data-ttu-id="6790b-155">Para ello, normalmente se agrega un punto y el número de versión al nombre.</span><span class="sxs-lookup"><span data-stu-id="6790b-155">You typically do this by adding a period and the version number to the name.</span></span> <span data-ttu-id="6790b-156">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="6790b-156">For example:</span></span>

-   <span data-ttu-id="6790b-157">Word.Document. 6</span><span class="sxs-lookup"><span data-stu-id="6790b-157">Word.Document.6</span></span>
-   <span data-ttu-id="6790b-158">Word.Document. 8</span><span class="sxs-lookup"><span data-stu-id="6790b-158">Word.Document.8</span></span>

<span data-ttu-id="6790b-159">Se trata de ProgID con versión, con las versiones 6 y 8, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="6790b-159">These are versioned ProgIDs, with versions 6 and 8 respectively.</span></span> <span data-ttu-id="6790b-160">Si tiene una aplicación en paralelo, es decir, una que admita varias versiones de la aplicación instaladas al mismo tiempo, use los ProgID independientes de curva y de versión.</span><span class="sxs-lookup"><span data-stu-id="6790b-160">If you have a side-by-side application, that is, one that supports multiple versions of your application installed at the same time, then use CurVer and Version Independent ProgIDs.</span></span> <span data-ttu-id="6790b-161">De lo contrario, deben evitarse los ProgID independientes de la versión y del curvador, ya que provocarán ineficiencias.</span><span class="sxs-lookup"><span data-stu-id="6790b-161">Otherwise, CurVer and Version Independent ProgIDs should be avoided because they will lead to inefficiency.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6790b-162">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6790b-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6790b-163">Cómo registrar un tipo de archivo para una nueva aplicación</span><span class="sxs-lookup"><span data-stu-id="6790b-163">How To Register a File Type for a New Application</span></span>](how-to-register-a-file-type-for-a-new-application.md)
</dt> <dt>

[<span data-ttu-id="6790b-164">Registro de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="6790b-164">Application Registration</span></span>](app-registration.md)
</dt> <dt>

[<span data-ttu-id="6790b-165">Tipos de archivo</span><span class="sxs-lookup"><span data-stu-id="6790b-165">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="6790b-166">Cómo funcionan las asociaciones de archivos</span><span class="sxs-lookup"><span data-stu-id="6790b-166">How File Associations Work</span></span>](fa-how-work.md)
</dt> <dt>

[<span data-ttu-id="6790b-167">Vista de contenido por tipo de archivo o tipo</span><span class="sxs-lookup"><span data-stu-id="6790b-167">Content View By File Type or Kind</span></span>](prophand-content-view.md)
</dt> <dt>

[<span data-ttu-id="6790b-168">Comprobador de tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="6790b-168">File Type Verifier</span></span>](file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="6790b-169">Controladores de tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="6790b-169">File Type Handlers</span></span>](fa-file-extensions.md)
</dt> <dt>

[<span data-ttu-id="6790b-170">Tipos percibidos</span><span class="sxs-lookup"><span data-stu-id="6790b-170">Perceived Types</span></span>](fa-perceivedtypes.md)
</dt> <dt>

[<span data-ttu-id="6790b-171">Matrices de asociación</span><span class="sxs-lookup"><span data-stu-id="6790b-171">Association Arrays</span></span>](fa-associationarray.md)
</dt> </dl>

 

 




