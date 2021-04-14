---
description: En este tema se explica cómo crear nuevos tipos de archivo y cómo asociar la aplicación con el tipo de archivo y otros tipos de archivo bien definidos.
ms.assetid: 055648cd-46ce-4e61-80b2-bcf1d1823e20
title: Tipos de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d697c42626c6e1ab3e0b5cc0b88bd065523d53a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985531"
---
# <a name="file-types"></a><span data-ttu-id="f4fc4-103">Tipos de archivo</span><span class="sxs-lookup"><span data-stu-id="f4fc4-103">File Types</span></span>

<span data-ttu-id="f4fc4-104">En este tema se explica cómo crear nuevos tipos de archivo y cómo asociar la aplicación con el tipo de archivo y otros tipos de archivo bien definidos.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-104">This topic explains how to create new file types and how to associate your app with your file type and other well-defined file types.</span></span> <span data-ttu-id="f4fc4-105">Los archivos con una extensión de nombre de archivo común compartida (. doc,. html, etc.) son del mismo *tipo*.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-105">Files with a shared common file name extension (.doc, .html, and so on) are of the same *type*.</span></span> <span data-ttu-id="f4fc4-106">Por ejemplo, si crea un nuevo editor de texto, puede usar el tipo de archivo. txt existente.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-106">For example, if you create a new text editor, then you can use the existing .txt file type.</span></span> <span data-ttu-id="f4fc4-107">En otros casos, puede que tenga que crear un nuevo tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-107">In other cases, you might need to create a new file type.</span></span>

<span data-ttu-id="f4fc4-108">Este tema se organiza de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="f4fc4-108">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="f4fc4-109">Tipos de archivo públicos y privados</span><span class="sxs-lookup"><span data-stu-id="f4fc4-109">Public and Private File Types</span></span>](#public-and-private-file-types)
-   [<span data-ttu-id="f4fc4-110">Registro de un tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="f4fc4-110">Registering a File Type</span></span>](#registering-a-file-type)
    -   [<span data-ttu-id="f4fc4-111">Establecer subclaves opcionales y atributos de extensión de tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="f4fc4-111">Setting Optional Subkeys and File Type Extension Attributes</span></span>](#setting-optional-subkeys-and-file-type-extension-attributes)
    -   [<span data-ttu-id="f4fc4-112">Eliminar información del registro durante la desinstalación</span><span class="sxs-lookup"><span data-stu-id="f4fc4-112">Deleting Registry Information During Uninstallation</span></span>](#deleting-registry-information-during-uninstallation)
-   [<span data-ttu-id="f4fc4-113">Tipos de archivo que admiten metadatos abiertos</span><span class="sxs-lookup"><span data-stu-id="f4fc4-113">File Types That Support Open Metadata</span></span>](#file-types-that-support-open-metadata)
-   [<span data-ttu-id="f4fc4-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f4fc4-114">Related topics</span></span>](#related-topics)

<span data-ttu-id="f4fc4-115">Puede encontrar información adicional en los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="f4fc4-115">Additional information can be found on the following topics:</span></span>

-   [<span data-ttu-id="f4fc4-116">Cómo elegir una extensión de tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="f4fc4-116">How To Choose a File Type Extension</span></span>](how-to-choose-a-file-type-extension.md)
-   [<span data-ttu-id="f4fc4-117">Cómo definir atributos de tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="f4fc4-117">How To Define File Type Attributes</span></span>](./how-to-define-file-type-attributes.md)
-   [<span data-ttu-id="f4fc4-118">Cómo incluir una aplicación en el cuadro de diálogo Abrir con</span><span class="sxs-lookup"><span data-stu-id="f4fc4-118">How To Include an Application on the Open with Dialog Box</span></span>](how-to-include-an-application-on-the-open-with-dialog-box.md)
-   [<span data-ttu-id="f4fc4-119">Cómo excluir una aplicación del cuadro de diálogo Abrir con para tipos de archivo no asociados</span><span class="sxs-lookup"><span data-stu-id="f4fc4-119">How To Exclude an Application from the Open with Dialog Box for Unassociated File Types</span></span>](how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types.md)

## <a name="public-and-private-file-types"></a><span data-ttu-id="f4fc4-120">Tipos de archivo públicos y privados</span><span class="sxs-lookup"><span data-stu-id="f4fc4-120">Public and Private File Types</span></span>

<span data-ttu-id="f4fc4-121">Los tipos de archivo públicos también se conocen como tipos populares o polémicos porque es posible que las aplicaciones competidoras quieran estar asociadas con estos tipos de archivo.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-121">Public file types are also known as popular or contentious types because competing applications might want to be associated with these file types.</span></span> <span data-ttu-id="f4fc4-122">Las características de los tipos de archivo públicos incluyen:</span><span class="sxs-lookup"><span data-stu-id="f4fc4-122">Characteristics of public file types include:</span></span>

-   <span data-ttu-id="f4fc4-123">Normalmente, se definen mediante cuerpos de estándares o se promocionan por sus organizaciones que la definen como formatos de intercambio.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-123">They are typically defined by standards bodies, and/or are promoted by their defining organizations as interchange formats.</span></span>
-   <span data-ttu-id="f4fc4-124">A menudo se intercambian entre equipos y usuarios para distintos fines.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-124">They are often exchanged between computers and users for diverse purposes.</span></span>
-   <span data-ttu-id="f4fc4-125">Deben admitirse en muchas plataformas diferentes.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-125">They need to be supported on many different platforms.</span></span>
-   <span data-ttu-id="f4fc4-126">Es probable que las aplicaciones de varios proveedores las controlen.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-126">Applications from multiple vendors are likely to handle them.</span></span>

<span data-ttu-id="f4fc4-127">Algunos ejemplos de tipos de archivo que se consideran públicos son los tipos de archivo de imagen. png,. gif,. jpg y. bmp, y los tipos de audio. wav,. mp3 y. au.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-127">Some examples of file types that are considered public are the image file types .png, .gif, .jpg, and .bmp, and the audio types .wav, .mp3, and .au.</span></span>

<span data-ttu-id="f4fc4-128">A diferencia de los tipos de archivo públicos, los tipos de archivos privados o propietarios suelen tener un formato que solo una aplicación o un proveedor comprenden.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-128">Unlike public file types, private or proprietary file types typically have a format that is implemented and understood by only one application or vendor.</span></span> <span data-ttu-id="f4fc4-129">Como resultado, los tipos de archivo privados no suelen ser propensos a conflictos entre aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-129">As a result, private file types are typically not prone to conflicts between applications.</span></span> <span data-ttu-id="f4fc4-130">Algunos tipos de archivo se pueden iniciar como tipos de archivo privados, pero posteriormente se convierten en tipos de archivo públicos.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-130">Some file types can start as private file types but later become public file types.</span></span>

> [!Note]  
> <span data-ttu-id="f4fc4-131">Windows no diferencia entre los tipos de archivo públicos y privados.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-131">Windows does not differentiate between public and private file types.</span></span> <span data-ttu-id="f4fc4-132">La distinción solo es relevante para tomar decisiones sobre la elección del registro de tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-132">The distinction is relevant only in making decisions about your choice of file type registration.</span></span>

 

## <a name="registering-a-file-type"></a><span data-ttu-id="f4fc4-133">Registro de un tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="f4fc4-133">Registering a File Type</span></span>

<span data-ttu-id="f4fc4-134">Para asociar el tipo de archivo a una aplicación existente, busque el ProgID de la aplicación en el registro.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-134">To associate the file type with an existing application, locate the application ProgID in the registry.</span></span> <span data-ttu-id="f4fc4-135">Para asociar el tipo de archivo a una nueva aplicación, defina un ProgID para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-135">To associate the file type with a new application, define a ProgID for your application.</span></span> <span data-ttu-id="f4fc4-136">Para obtener información sobre cómo definir un nuevo ProgID, vea [identificadores de programación](fa-progids.md).</span><span class="sxs-lookup"><span data-stu-id="f4fc4-136">For information about defining a new ProgID, see [Programmatic Identifiers](fa-progids.md).</span></span>

<span data-ttu-id="f4fc4-137">Las subclaves de la extensión de nombre de archivo tienen el formato general siguiente: ProgID de *extensión* = .</span><span class="sxs-lookup"><span data-stu-id="f4fc4-137">File name extension subkeys have the following general form: *extension*=*ProgID*.</span></span> <span data-ttu-id="f4fc4-138">Las subclaves de extensión de nombre de archivo se almacenan en el subárbol **\_ \_ raíz de las clases HKEY** .</span><span class="sxs-lookup"><span data-stu-id="f4fc4-138">File name extension subkeys are stored in the **HKEY\_CLASSES\_ROOT** subtree.</span></span>

<span data-ttu-id="f4fc4-139">Es importante incluir el punto inicial (.) al crear subclaves de tipo de archivo en el registro.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-139">It is important to include the leading period (.) when creating file type subkeys in the registry.</span></span> <span data-ttu-id="f4fc4-140">Por ejemplo, si desea que un tipo de archivo con la extensión abreviada. MYP y el archivo Long Extension. MYP se abra con una aplicación llamada, use la siguiente sintaxis:</span><span class="sxs-lookup"><span data-stu-id="f4fc4-140">For example, if you want a file type with the short extension .myp and the long extension .myp-file to be opened with an application called MyProgram, use the following syntax:</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = ApplicationVendor.MyProgram
   .myp-file
      (Default) = ApplicationVendor.MyProgram
   ApplicationVendor.MyProgram
      (Default) = MyProgram Application
```

<span data-ttu-id="f4fc4-141">Como se muestra en el ejemplo anterior, si también registra una extensión de nombre de archivo corto (. MYP), debe crear una subclave para la extensión larga (. MYP-File) también.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-141">As demonstrated in the preceding example, if you also register a short file name extension (.myp), you should create a subkey for the long extension (.myp-file) as well.</span></span> <span data-ttu-id="f4fc4-142">Para obtener más información, vea [controladores de tipo de archivo](fa-file-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="f4fc4-142">For more information, see [File Type Handlers](fa-file-extensions.md).</span></span>

### <a name="setting-optional-subkeys-and-file-type-extension-attributes"></a><span data-ttu-id="f4fc4-143">Establecer subclaves opcionales y atributos de extensión de tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="f4fc4-143">Setting Optional Subkeys and File Type Extension Attributes</span></span>

<span data-ttu-id="f4fc4-144">Las entradas de extensión de tipo de archivo del registro tienen varias subclaves y atributos opcionales.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-144">File type extension entries in the registry have several optional subkeys and attributes.</span></span>

<span data-ttu-id="f4fc4-145">En la tabla siguiente se describen las entradas de extensión de tipo de archivo que se usan en las asociaciones de archivo.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-145">The file type extension entries that are used by file associations are described in the following table.</span></span> <span data-ttu-id="f4fc4-146">Todos los valores son del tipo **reg \_ SZ** .</span><span class="sxs-lookup"><span data-stu-id="f4fc4-146">All values are of the **REG\_SZ** type.</span></span>



| <span data-ttu-id="f4fc4-147">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="f4fc4-147">Registry entry</span></span>  | <span data-ttu-id="f4fc4-148">Acción</span><span class="sxs-lookup"><span data-stu-id="f4fc4-148">Action</span></span>                                                                                                                                                                                                                                                                                                                             |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4fc4-149">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="f4fc4-149">Default</span></span>         | <span data-ttu-id="f4fc4-150">Establezca el valor predeterminado de la subclave de extensión en el ProgID al que está vinculado.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-150">Set the default value of the extension subkey to the ProgID to which it is linked.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="f4fc4-151">Tipo de contenido</span><span class="sxs-lookup"><span data-stu-id="f4fc4-151">Content Type</span></span>    | <span data-ttu-id="f4fc4-152">Establezca el valor de tipo de contenido en el tipo de contenido MIME del tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-152">Set the Content Type value to the file type's MIME content type.</span></span>                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="f4fc4-153">OpenWithList</span><span class="sxs-lookup"><span data-stu-id="f4fc4-153">OpenWithList</span></span>    | <span data-ttu-id="f4fc4-154">No debe usarse.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-154">Do not use.</span></span> <span data-ttu-id="f4fc4-155">Esta subclave contiene una o más subclaves de aplicación para las aplicaciones que aparecen en la entrada del cuadro de diálogo **abrir con** para el tipo de archivo y se ha diseñado únicamente para aplicaciones. exe en sistemas operativos anteriores a Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-155">This subkey contains one or more application subkeys for applications that appear in the **Open with** dialog box entry for the file type and is intended only for .exe applications on operating systems prior to Windows XP.</span></span> <span data-ttu-id="f4fc4-156">Use OpenWithProgIds en su lugar.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-156">Use OpenWithProgIds instead.</span></span>                                                            |
| <span data-ttu-id="f4fc4-157">OpenWithProgIds</span><span class="sxs-lookup"><span data-stu-id="f4fc4-157">OpenWithProgIds</span></span> | <span data-ttu-id="f4fc4-158">Esta subclave contiene una lista de ProgID alternativos para este tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-158">This subkey contains a list of alternate ProgIDs for this file type.</span></span> <span data-ttu-id="f4fc4-159">Los programas de estos ProgID aparecen en el menú **abrir con** y están disponibles como aplicaciones de la tienda Windows predeterminadas para el tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-159">The programs for these ProgIDs appear in the **Open with** menu and are available as default Windows Store apps for the file type.</span></span> <span data-ttu-id="f4fc4-160">Cada vez que una aplicación usa este tipo de archivo cambiando el valor predeterminado, también debe agregar una entrada a esta lista.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-160">Whenever an application takes over this file type by changing the default value, it should also add an entry to this list.</span></span> |
| <span data-ttu-id="f4fc4-161">PerceivedType</span><span class="sxs-lookup"><span data-stu-id="f4fc4-161">PerceivedType</span></span>   | <span data-ttu-id="f4fc4-162">Establezca el valor de PerceivedType en el PerceivedType al que pertenece el archivo, si existe.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-162">Set the PerceivedType value to the PerceivedType to which the file belongs, if any.</span></span> <span data-ttu-id="f4fc4-163">Las versiones de Windows anteriores a Windows Vista no utilizan esta cadena.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-163">This string is not used by Windows versions prior to Windows Vista.</span></span> <span data-ttu-id="f4fc4-164">Para obtener más información, vea [tipos percibidos y registro de aplicaciones](fa-perceivedtypes.md).</span><span class="sxs-lookup"><span data-stu-id="f4fc4-164">For more information, see [Perceived Types and Application Registration](fa-perceivedtypes.md).</span></span>                                                                           |



 

<span data-ttu-id="f4fc4-165">La forma general de una subclave de extensión de nombre de archivo es la siguiente.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-165">The general form of a file name extension subkey is as follows.</span></span> <span data-ttu-id="f4fc4-166">Todos los tipos de entrada son del tipo **reg \_ SZ** .</span><span class="sxs-lookup"><span data-stu-id="f4fc4-166">All entry types are of the **REG\_SZ** type.</span></span>

```
HKEY_CLASSES_ROOT
   .ext
      (Default) = ProgID.ext.1
      Content Type = MIME content type
      PerceivedType = PerceivedType
      OpenWithProgids
         ProgID2.ext.1
         ProgID3.ext.1
      ProgID.ext.1
         shellnew
```

<span data-ttu-id="f4fc4-167">Las consideraciones importantes sobre los tipos de archivo incluyen:</span><span class="sxs-lookup"><span data-stu-id="f4fc4-167">Important considerations about file types include:</span></span>

-   <span data-ttu-id="f4fc4-168">El subárbol **\_ \_ raíz de las clases HKEY** es una vista formada mediante la combinación de las clases de software de **\_ \_ usuario actual** \\  \\  de HKEY y las clases de software de **\_ \_ máquina local HKEY** \\  \\ </span><span class="sxs-lookup"><span data-stu-id="f4fc4-168">The **HKEY\_CLASSES\_ROOT** subtree is a view formed by merging **HKEY\_CURRENT\_USER**\\**Software**\\**Classes** and **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Classes**</span></span>
-   <span data-ttu-id="f4fc4-169">En general, **la \_ \_ raíz de las clases HKEY** está pensada para que se pueda leer, pero no se puede escribir en ella.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-169">In general, **HKEY\_CLASSES\_ROOT** is intended to be read from but not written to.</span></span> <span data-ttu-id="f4fc4-170">Para obtener más información, consulte el artículo [ \_ \_ raíz de clases HKEY](../sysinfo/hkey-classes-root-key.md) .</span><span class="sxs-lookup"><span data-stu-id="f4fc4-170">For more information, see the [HKEY\_CLASSES\_ROOT](../sysinfo/hkey-classes-root-key.md) article.</span></span>
-   <span data-ttu-id="f4fc4-171">Para registrar un tipo de archivo globalmente en un equipo determinado, cree una entrada para el tipo de archivo en la subclave **HKEY \_ local \_ Machine** \\ **software** \\ **classes** .</span><span class="sxs-lookup"><span data-stu-id="f4fc4-171">To register a file type globally on a particular computer, create an entry for the file type in the **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Classes** subkey.</span></span>
-   <span data-ttu-id="f4fc4-172">Para que un registro de tipo de archivo sea visible solo para el usuario actual, cree una entrada para el tipo de archivo en la subclave de clases de software del **\_ \_ usuario actual de HKEY** \\  \\  .</span><span class="sxs-lookup"><span data-stu-id="f4fc4-172">To make a file type registration visible to the current user only, create an entry for the file type in the **HKEY\_CURRENT\_USER**\\**Software**\\**Classes** subkey.</span></span>
-   <span data-ttu-id="f4fc4-173">Una aplicación puede proporcionar su propia implementación de un verbo, como Open o Play, como se muestra en el siguiente ejemplo del registro.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-173">An application can provide its own implementation of a verb, such as open or play, as shown in the following registry example.</span></span>

    ```
    HKEY_CLASSES_ROOT
       Applications
          ApplicationName.exe
             shell
                verb
    ```

    <span data-ttu-id="f4fc4-174">Las subclaves de la subclave Verb incluyen la línea de comandos y el método de destino de colocación: **Command** y **DropTarget**.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-174">Subkeys of the verb subkey include the command line and the drop target method: **command** and **DropTarget**.</span></span>

-   <span data-ttu-id="f4fc4-175">Al crear o cambiar una asociación de archivo, es importante notificar al sistema que ha realizado un cambio.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-175">When you create or change a file association, it is important to notify the system that you have made a change.</span></span> <span data-ttu-id="f4fc4-176">Para ello, llame a [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) y especifique el **evento \_ ASSOCCHANGED de SHCNE** .</span><span class="sxs-lookup"><span data-stu-id="f4fc4-176">Do so by calling [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) and specifying the **SHCNE\_ASSOCCHANGED** event.</span></span> <span data-ttu-id="f4fc4-177">Si no llama a **SHChangeNotify**, es posible que no se reconozca el cambio hasta que se reinicie el sistema.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-177">If you do not call **SHChangeNotify**, the change may not be recognized until after the system is rebooted.</span></span>
-   <span data-ttu-id="f4fc4-178">Para recuperar información del registro relativa a una asociación de archivo, use la interfaz [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) .</span><span class="sxs-lookup"><span data-stu-id="f4fc4-178">To retrieve registry information regarding a file association, use the [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) interface.</span></span> <span data-ttu-id="f4fc4-179">Para ver un escenario que ilustra este procedimiento, consulte el [escenario de ejemplo de Asociación de archivos](fa-sample-scenarios.md).</span><span class="sxs-lookup"><span data-stu-id="f4fc4-179">For a scenario that illustrates this procedure, see [File Association Sample Scenario](fa-sample-scenarios.md).</span></span>

> [!Note]  
> <span data-ttu-id="f4fc4-180">Las subclaves del registro de **aplicaciones** y rutas de acceso de la **aplicación** se usan para registrar y controlar el comportamiento del sistema en nombre de las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-180">Both the **App Paths** and **Applications** registry subkeys are used to register and control the behavior of the system on behalf of applications.</span></span> <span data-ttu-id="f4fc4-181">Para obtener información más detallada sobre esta funcionalidad, consulte [registro de aplicaciones](app-registration.md).</span><span class="sxs-lookup"><span data-stu-id="f4fc4-181">For more detailed information about this functionality, see [Application Registration](app-registration.md).</span></span>

 

### <a name="deleting-registry-information-during-uninstallation"></a><span data-ttu-id="f4fc4-182">Eliminar información del registro durante la desinstalación</span><span class="sxs-lookup"><span data-stu-id="f4fc4-182">Deleting Registry Information During Uninstallation</span></span>

<span data-ttu-id="f4fc4-183">Al desinstalar una aplicación, los ProgID y la mayoría de la información del registro asociada a esa aplicación deben eliminarse como parte de la desinstalación.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-183">When uninstalling an application, the ProgIDs and most other registry information associated with that application should be deleted as part of the uninstallation.</span></span> <span data-ttu-id="f4fc4-184">Sin embargo, las aplicaciones que han tomado posesión de un tipo de archivo (estableciendo el valor predeterminado de la subclave **\_ \_ raíz**. Extension del tipo de archivo \\  en el identificador de programa de la aplicación) no deben intentar quitar ese valor al desinstalar.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-184">However, applications that have taken ownership of a file type (by setting the Default value of the file type's **HKEY\_CLASSES\_ROOT**\\ *.extension* subkey to the ProgID of the application) should not attempt to remove that value when uninstalling.</span></span> <span data-ttu-id="f4fc4-185">Si se dejan los datos en su lugar para el valor predeterminado, se evita la dificultad de determinar si otra aplicación ha tomado posesión del tipo de archivo y se ha sobrescrito el valor predeterminado después de instalar la aplicación original.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-185">Leaving the data in place for the Default value avoids the difficulty of determining whether another application has taken ownership of the file type and overwritten the Default value after the original application was installed.</span></span> <span data-ttu-id="f4fc4-186">Windows respeta el valor predeterminado solo si el identificador de programa (ProgID) encuentra un ProgID registrado.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-186">Windows respects the Default value only if the ProgID found there is a registered ProgID.</span></span> <span data-ttu-id="f4fc4-187">Si se anula el registro del ProgID, se omite.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-187">If the ProgID is unregistered, it is ignored.</span></span>

<span data-ttu-id="f4fc4-188">Tenga en cuenta que la información de propiedad de tipo de archivo se almacena en el subárbol de **\_ \_ usuario de HKEY actual** y que también se usa solo cuando se registra la aplicación a la que hace referencia.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-188">Note that other file-type ownership information is stored in the **HKEY\_CURRENT\_USER** subtree and also is used only when the application that it references is registered.</span></span> <span data-ttu-id="f4fc4-189">Por lo tanto, no es necesario quitar estos datos al desinstalar una aplicación.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-189">Therefore, this data does not need to be removed when uninstalling an application.</span></span>

<span data-ttu-id="f4fc4-190">Como ejemplo, a continuación se muestra el estado del registro antes de que se desinstale una aplicación:</span><span class="sxs-lookup"><span data-stu-id="f4fc4-190">As an example, the following shows the state of the registry before an application is uninstalled:</span></span>

```
HKEY_CLASSES_ROOT
   .mp3
      (Default) = YourProgID
   YourProgID
      shell
         open
            command
               (Default) = yourapp.exe %1
```

<span data-ttu-id="f4fc4-191">A continuación se muestra el estado de las mismas entradas del registro después de desinstalar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-191">The following shows the state of those same registry entries after the application has been uninstalled.</span></span>

```
HKEY_CLASSES_ROOT
   .mp3
      (Default) = YourProgID
   YourProgID subkey removed
```

## <a name="file-types-that-support-open-metadata"></a><span data-ttu-id="f4fc4-192">Tipos de archivo que admiten metadatos abiertos</span><span class="sxs-lookup"><span data-stu-id="f4fc4-192">File Types That Support Open Metadata</span></span>

<span data-ttu-id="f4fc4-193">En Windows 7 y versiones posteriores, los siguientes tipos de archivo admiten metadatos abiertos.</span><span class="sxs-lookup"><span data-stu-id="f4fc4-193">In Windows 7 and later, the following file types support open metadata.</span></span>



| <span data-ttu-id="f4fc4-194">Tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="f4fc4-194">File type</span></span>                                                               | <span data-ttu-id="f4fc4-195">Extensiones de nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="f4fc4-195">File name extensions</span></span>                                          |
|-------------------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="f4fc4-196">Documentos de Office 2007</span><span class="sxs-lookup"><span data-stu-id="f4fc4-196">Office 2007 Documents</span></span>                                                   | <span data-ttu-id="f4fc4-197">. docx,. xlsx y. pptx</span><span class="sxs-lookup"><span data-stu-id="f4fc4-197">.docx, .xlsx, .pptx</span></span>                                           |
| <span data-ttu-id="f4fc4-198">Documentos de Office 97-2003</span><span class="sxs-lookup"><span data-stu-id="f4fc4-198">Office 97-2003 Documents</span></span>                                                | <span data-ttu-id="f4fc4-199">. doc,. xls,. ppt</span><span class="sxs-lookup"><span data-stu-id="f4fc4-199">.doc, .xls, .ppt</span></span>                                              |
| <span data-ttu-id="f4fc4-200">Búsqueda guardada</span><span class="sxs-lookup"><span data-stu-id="f4fc4-200">Saved Search</span></span>                                                            | <span data-ttu-id="f4fc4-201">. Search-MS</span><span class="sxs-lookup"><span data-stu-id="f4fc4-201">.search-ms</span></span>                                                    |
| <span data-ttu-id="f4fc4-202">Formatos basados en Windows Media (contenedor ASF)</span><span class="sxs-lookup"><span data-stu-id="f4fc4-202">Windows Media-based formats (Advanced Streaming Format (ASF) container)</span></span> | <span data-ttu-id="f4fc4-203">. wmv,. WMA</span><span class="sxs-lookup"><span data-stu-id="f4fc4-203">.wmv, .wma</span></span>                                                    |
| <span data-ttu-id="f4fc4-204">MP4 (controlador de propiedades)</span><span class="sxs-lookup"><span data-stu-id="f4fc4-204">MP4 (property handler)</span></span>                                                  | <span data-ttu-id="f4fc4-205">. MP4,. m4a,. M4V,. MP4V,. M4P,. M4B,. 3GP,. 3GPP,. 3GP2,. mov</span><span class="sxs-lookup"><span data-stu-id="f4fc4-205">.mp4, .m4a, .m4v, .mp4v, .m4p, .m4b, .3gp, .3gpp, .3gp2, .mov</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="f4fc4-206">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f4fc4-206">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4fc4-207">Registro de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="f4fc4-207">Application Registration</span></span>](app-registration.md)
</dt> <dt>

[<span data-ttu-id="f4fc4-208">Cómo funcionan las asociaciones de archivos</span><span class="sxs-lookup"><span data-stu-id="f4fc4-208">How File Associations Work</span></span>](fa-how-work.md)
</dt> <dt>

[<span data-ttu-id="f4fc4-209">Vista de contenido por tipo de archivo o tipo</span><span class="sxs-lookup"><span data-stu-id="f4fc4-209">Content View By File Type or Kind</span></span>](prophand-content-view.md)
</dt> <dt>

[<span data-ttu-id="f4fc4-210">Comprobador de tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="f4fc4-210">File Type Verifier</span></span>](file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="f4fc4-211">Controladores de tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="f4fc4-211">File Type Handlers</span></span>](fa-file-extensions.md)
</dt> <dt>

[<span data-ttu-id="f4fc4-212">Identificadores de programación</span><span class="sxs-lookup"><span data-stu-id="f4fc4-212">Programmatic Identifiers</span></span>](fa-progids.md)
</dt> <dt>

[<span data-ttu-id="f4fc4-213">Tipos percibidos</span><span class="sxs-lookup"><span data-stu-id="f4fc4-213">Perceived Types</span></span>](fa-perceivedtypes.md)
</dt> <dt>

[<span data-ttu-id="f4fc4-214">Matrices de asociación</span><span class="sxs-lookup"><span data-stu-id="f4fc4-214">Association Arrays</span></span>](fa-associationarray.md)
</dt> </dl>

 

 
