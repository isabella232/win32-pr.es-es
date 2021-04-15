---
description: El almacenamiento de cadenas codificadas de forma rígida en el registro forma parte de un modelo de localización anterior a Windows Vista.
ms.assetid: 70185942-7d32-4151-a4e1-f71cf45e87af
title: Usar el redireccionamiento de cadenas del registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 287f6e1420aae0ff41c386e19852bebbd1a322c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688692"
---
# <a name="using-registry-string-redirection"></a><span data-ttu-id="393fa-103">Usar el redireccionamiento de cadenas del registro</span><span class="sxs-lookup"><span data-stu-id="393fa-103">Using Registry String Redirection</span></span>

<span data-ttu-id="393fa-104">El almacenamiento de cadenas codificadas de forma rígida en el registro forma parte de un modelo de localización anterior a Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="393fa-104">Storage of hard-coded strings in the registry is part of a pre-Windows Vista localization model.</span></span> <span data-ttu-id="393fa-105">No es compatible con MUI.</span><span class="sxs-lookup"><span data-stu-id="393fa-105">It is not supported by MUI.</span></span> <span data-ttu-id="393fa-106">En el modelo actual, la interfaz de usuario del sistema operativo se ejecuta en archivos de recursos específicos del idioma encima de una base independiente del lenguaje.</span><span class="sxs-lookup"><span data-stu-id="393fa-106">In the current model, the user interface for the operating system runs in language-specific resource files on top of a language-neutral base.</span></span> <span data-ttu-id="393fa-107">Los componentes del sistema operativo utilizan el registro de forma independiente del idioma.</span><span class="sxs-lookup"><span data-stu-id="393fa-107">The components of the operating system use the registry in a language-neutral manner.</span></span>

<span data-ttu-id="393fa-108">MUI solo usa cadenas de registro redirigidas definidas por recursos PE de Win32 en el archivo de recursos de idioma base.</span><span class="sxs-lookup"><span data-stu-id="393fa-108">MUI uses only redirected registry strings defined by Win32 PE resources in the base language resource file.</span></span> <span data-ttu-id="393fa-109">La redirección se define por separado, por ejemplo, en un archivo. inf.</span><span class="sxs-lookup"><span data-stu-id="393fa-109">Redirection is defined separately, for example, in an .inf file.</span></span> <span data-ttu-id="393fa-110">Este tipo de almacenamiento permite al cargador de recursos seleccionar automáticamente los recursos de idioma correctos durante la carga del módulo de recursos.</span><span class="sxs-lookup"><span data-stu-id="393fa-110">This type of storage allows the resource loader to select the correct language resources automatically during resource module loading.</span></span>

> [!Note]  
> <span data-ttu-id="393fa-111">Este tema solo pertenece a los recursos de Win32 PE.</span><span class="sxs-lookup"><span data-stu-id="393fa-111">This topic pertains only to Win32 PE resources.</span></span> <span data-ttu-id="393fa-112">Si utiliza recursos de PE que no son de Win32, debe proporcionar redirección de cadenas del registro personalizada, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="393fa-112">If using non-Win32 PE resources, you must provide customized registry string redirection, if required.</span></span>

 

## <a name="create-a-language-neutral-resource"></a><span data-ttu-id="393fa-113">Creación de un recurso de Language-Neutral</span><span class="sxs-lookup"><span data-stu-id="393fa-113">Create a Language-Neutral Resource</span></span>

<span data-ttu-id="393fa-114">Una aplicación MUI que se ejecuta en Windows Vista y versiones posteriores usa un recurso de cadena independiente del lenguaje para permitir el acceso a cadenas específicas del idioma almacenadas en una tabla de recursos de cadena.</span><span class="sxs-lookup"><span data-stu-id="393fa-114">A MUI application running on Windows Vista and later uses a language-neutral string resource to allow access to language-specific strings stored in a string resource table.</span></span> <span data-ttu-id="393fa-115">El código de la aplicación que lee estos valores del registro se describe en la sección carga de un valor de registro de Language-Neutral de [búsqueda de cadenas redirigidas](locating-redirected-strings.md).</span><span class="sxs-lookup"><span data-stu-id="393fa-115">Application code that reads these values from the registry is described in the Load a Language-Neutral Registry Value section of [Locating Redirected Strings](locating-redirected-strings.md).</span></span>

<span data-ttu-id="393fa-116">Los datos de un valor del registro independiente del lenguaje tienen el formato " `@<PE-path>,-<stringID>[;<comment>]` ", donde:</span><span class="sxs-lookup"><span data-stu-id="393fa-116">The data for a language-neutral registry value has the format "`@<PE-path>,-<stringID>[;<comment>]`", where:</span></span>

-   <span data-ttu-id="393fa-117">*PE-path* especifica la ruta de acceso del archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="393fa-117">*PE-path* specifies the path of the executable.</span></span> <span data-ttu-id="393fa-118">Puede especificar la ruta de acceso mediante una variable de entorno, como% ProgramFiles%, para admitir la implementación.</span><span class="sxs-lookup"><span data-stu-id="393fa-118">You can specify the path using an environment variable, such as %ProgramFiles%, to support deployment.</span></span> <span data-ttu-id="393fa-119">Una alternativa para hacer referencia a la cadena es omitir la información de la ruta de acceso del archivo.</span><span class="sxs-lookup"><span data-stu-id="393fa-119">An alternative for making your string reference is to leave out the file path information.</span></span> <span data-ttu-id="393fa-120">En este caso, la aplicación debe tener algunos medios, por ejemplo, otro valor del registro, para comunicar su propio directorio de instalación.</span><span class="sxs-lookup"><span data-stu-id="393fa-120">In this case, your application must have some means, for example, another registry value, to communicate its own install directory.</span></span>
-   <span data-ttu-id="393fa-121">*stringID* especifica el identificador de recursos numérico del recurso de cadena pertinente, que se implementa igual que cualquier otro recurso de cadena localizable.</span><span class="sxs-lookup"><span data-stu-id="393fa-121">*stringID* specifies the numeric resource identifier of the relevant string resource, which is implemented just like any other localizable string resource.</span></span>
-   <span data-ttu-id="393fa-122">*Comentario* especifica información opcional para la depuración o la legibilidad del valor del registro.</span><span class="sxs-lookup"><span data-stu-id="393fa-122">*comment* specifies optional information for debugging or readability of the registry value.</span></span> <span data-ttu-id="393fa-123">Las funciones de la API del registro omiten el comentario al cargar la cadena.</span><span class="sxs-lookup"><span data-stu-id="393fa-123">The registry API functions ignore the comment when loading the string.</span></span>

> [!Note]  
> <span data-ttu-id="393fa-124">Los datos para el valor del registro no hacen referencia explícita al archivo de recursos específico del lenguaje.</span><span class="sxs-lookup"><span data-stu-id="393fa-124">The data for the registry value makes no explicit reference to the language-specific resource file.</span></span> <span data-ttu-id="393fa-125">El archivo correcto se determina en tiempo de ejecución, según las preferencias de idioma de la interfaz de usuario actual.</span><span class="sxs-lookup"><span data-stu-id="393fa-125">The correct file is determined at runtime, based on the current user interface language preferences.</span></span>

 

<span data-ttu-id="393fa-126">Un valor del registro se escribe sin un espacio entre "," y "-".</span><span class="sxs-lookup"><span data-stu-id="393fa-126">A registry value is entered without a space between the "," and "-".</span></span> <span data-ttu-id="393fa-127">Un valor del registro correcto es:</span><span class="sxs-lookup"><span data-stu-id="393fa-127">A correct registry value is:</span></span>

`shell32.dll,-22912`

<span data-ttu-id="393fa-128">Un valor de registro incorrecto es:</span><span class="sxs-lookup"><span data-stu-id="393fa-128">An incorrect registry value is:</span></span>

`shell32.dll, -22912`

<span data-ttu-id="393fa-129">Un ejemplo de Windows Vista es el valor del registro con los datos siguientes:</span><span class="sxs-lookup"><span data-stu-id="393fa-129">An example from Windows Vista is the registry value with the following data:</span></span>

`@%SystemRoot%\system32\input.dll,-5020`

## <a name="create-resources-for-shortcut-strings"></a><span data-ttu-id="393fa-130">Crear recursos para cadenas de acceso directo</span><span class="sxs-lookup"><span data-stu-id="393fa-130">Create Resources for Shortcut Strings</span></span>

<span data-ttu-id="393fa-131">Cuando la aplicación MUI muestra su nombre en la interfaz de usuario de Shell, se muestra una cadena de recuadro informativo para el icono de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="393fa-131">When the MUI application displays its name in the shell user interface, an InfoTip string is displayed for the application icon.</span></span> <span data-ttu-id="393fa-132">Debe crear recursos de cadena para el nombre para mostrar de la aplicación y la cadena de recuadro informativa asociada para cada idioma admitido.</span><span class="sxs-lookup"><span data-stu-id="393fa-132">You should create string resources for your application display name and associated InfoTip string for each supported language.</span></span> <span data-ttu-id="393fa-133">Cuando los recursos estén listos, la aplicación puede usar las cadenas tal y como se describe en la sección uso de la API de Shell para cargar cadenas de acceso directo desde el registro de [búsqueda de cadenas redirigidas](locating-redirected-strings.md).</span><span class="sxs-lookup"><span data-stu-id="393fa-133">When the resources are ready, your application can use the strings as described in the Use Shell API to Load Shortcut Strings from the Registry section of [Locating Redirected Strings](locating-redirected-strings.md).</span></span>

### <a name="prepare-resources-for-a-shortcut-created-with-windows-installer"></a><span data-ttu-id="393fa-134">Preparar los recursos de un acceso directo creado con Windows Installer</span><span class="sxs-lookup"><span data-stu-id="393fa-134">Prepare Resources for a Shortcut Created with Windows Installer</span></span>

<span data-ttu-id="393fa-135">Si usa Windows Installer (MSI) para crear un acceso directo, los recursos de cadena incluyen el nombre para mostrar y la descripción del método abreviado.</span><span class="sxs-lookup"><span data-stu-id="393fa-135">If you use Windows Installer (MSI) to create a shortcut, string resources include shortcut display name and description.</span></span> <span data-ttu-id="393fa-136">En la [tabla de accesos directos MSI](../msi/shortcut-table.md), se hace referencia a la dll de recursos en las columnas adecuadas y se usan los identificadores de recursos para el nombre para mostrar y la descripción del acceso directo en las columnas de identificador de recursos correspondientes.</span><span class="sxs-lookup"><span data-stu-id="393fa-136">In the [MSI shortcut table](../msi/shortcut-table.md), the resource DLL is referenced in the appropriate columns and the resource identifiers for your shortcut display name and description are used in the corresponding resource identifier columns.</span></span>

<span data-ttu-id="393fa-137">Para que el acceso directo de la aplicación funcione correctamente con la tecnología de recursos de MUI, tenga en cuenta los siguientes puntos al preparar las cadenas de acceso directo:</span><span class="sxs-lookup"><span data-stu-id="393fa-137">So that the application shortcut works properly with MUI resource technology, keep the following points in mind when preparing the shortcut strings:</span></span>

-   <span data-ttu-id="393fa-138">Use las variables de entorno o una ruta de acceso relativa para registrar el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="393fa-138">Use either environment variables or a relative path to register the DLL.</span></span> <span data-ttu-id="393fa-139">Puede especificar @% SystemRoot% \\ system32shell32.dll siempre que \\ el tipo de cadena del registro sea reg \_ Expand \_ SZ.</span><span class="sxs-lookup"><span data-stu-id="393fa-139">You can specify @%systemroot%\\system32\\shell32.dll as long as the registry string type is REG\_EXPAND\_SZ.</span></span> <span data-ttu-id="393fa-140">El identificador de recursos de cadena para "documento de texto" en Shell32.dll es 12345.</span><span class="sxs-lookup"><span data-stu-id="393fa-140">The string resource identifier for "Text Document" in Shell32.dll is 12345.</span></span>
-   <span data-ttu-id="393fa-141">No use espacios alrededor de los símbolos "," y "-".</span><span class="sxs-lookup"><span data-stu-id="393fa-141">Do not use spaces around the "," and "-" symbols.</span></span> <span data-ttu-id="393fa-142">Un ejemplo correcto es "shell32.dll,-22912".</span><span class="sxs-lookup"><span data-stu-id="393fa-142">A correct example is "shell32.dll,-22912".</span></span>
-   <span data-ttu-id="393fa-143">No use un nombre de archivo corto.</span><span class="sxs-lookup"><span data-stu-id="393fa-143">Do not use a short file name.</span></span> <span data-ttu-id="393fa-144">Este tipo de nombre no funciona con el cargador de recursos.</span><span class="sxs-lookup"><span data-stu-id="393fa-144">This type of name does not work with the resource loader.</span></span>

### <a name="prepare-resources-for-a-shortcut-using-inf-format"></a><span data-ttu-id="393fa-145">Preparar los recursos de un acceso directo mediante el formato INF</span><span class="sxs-lookup"><span data-stu-id="393fa-145">Prepare Resources for a Shortcut Using INF Format</span></span>

<span data-ttu-id="393fa-146">Si usa el formato de archivo INF para crear cadenas de acceso directo, el archivo de recursos debe tener la siguiente configuración del registro.</span><span class="sxs-lookup"><span data-stu-id="393fa-146">If you use the INF file format to create shortcut strings, the resource file should make the following registry settings.</span></span> <span data-ttu-id="393fa-147">En estas instrucciones se asume el uso de la sintaxis ProfileItems de la API de instalación.</span><span class="sxs-lookup"><span data-stu-id="393fa-147">These instructions assume the use of the ProfileItems syntax of Setup API.</span></span>

1.  <span data-ttu-id="393fa-148">Cambie el valor de recuadro informativo para que apunte a la referencia de redirección de cadenas mediante la ruta de acceso y el identificador de recursos.</span><span class="sxs-lookup"><span data-stu-id="393fa-148">Change the InfoTip value to point to the string redirection reference, using the path and resource identifier.</span></span>
2.  <span data-ttu-id="393fa-149">Agregue el nuevo valor DisplayResource en las secciones de instalación ProfileItems.</span><span class="sxs-lookup"><span data-stu-id="393fa-149">Add the new value DisplayResource under the ProfileItems installation sections.</span></span>

<span data-ttu-id="393fa-150">El siguiente es un ejemplo que muestra la adición de la aplicación Calculator al menú **Inicio** :</span><span class="sxs-lookup"><span data-stu-id="393fa-150">The following is an example showing the addition of the Calculator application to the **Start** menu:</span></span>


```C++
[CalcInstallItems]
"Name" = %Calc_DESC%
"CmdLine" = 11, calc.exe
"SubDir" = %Access_GROUP%
"WorkingDir" = 11

"InfoTip" = "@%systemroot%\system32\shell32.dll,-22531"

"DisplayResource" = "%systemroot%\system32\shell32.dll",22019
```



<span data-ttu-id="393fa-151">Use la sintaxis que se muestra a continuación al usar el archivo INF para agregar elementos, por ejemplo, una carpeta del grupo de acceso, al menú **Inicio** .</span><span class="sxs-lookup"><span data-stu-id="393fa-151">Use the syntax shown below when using INF to add items, for example, an Access Group folder, to the **Start** menu.</span></span> <span data-ttu-id="393fa-152">Esta sintaxis presupone el uso de \[ la \] compatibilidad con StartMenuItems del programa de instalación, similar a la sintaxis usada en Syssetup. inf.</span><span class="sxs-lookup"><span data-stu-id="393fa-152">This syntax assumes the use of \[StartMenuItems\] support from Setup, similar to the syntax used in Syssetup.inf.</span></span>


```C++
[StartMenuItems]
<description> = <binary>,<commandline>,<iconfile>,<iconnum>,<infotip>,<resDLL,resID>
```



<span data-ttu-id="393fa-153">Establezca *el valor de* recuadro informativo en la referencia de cadena " `@<path>,-resID` ".</span><span class="sxs-lookup"><span data-stu-id="393fa-153">Set the value *infotip* to the string reference "`@<path>,-resID`".</span></span>

<span data-ttu-id="393fa-154">Los valores *resDLL* y *resID* determinan el nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="393fa-154">The display name is determined by the *resDLL* and *resID* values.</span></span> <span data-ttu-id="393fa-155">El valor *resID* especifica el identificador de recurso para un recurso de cadena asociado con el archivo independiente del idioma.</span><span class="sxs-lookup"><span data-stu-id="393fa-155">The *resID* value specifies the resource identifier for a string resource associated with the language-neutral file.</span></span> <span data-ttu-id="393fa-156">El valor *resDLL* especifica la ruta de acceso al archivo independiente del idioma.</span><span class="sxs-lookup"><span data-stu-id="393fa-156">The *resDLL* value specifies the path to the language-neutral file.</span></span>

## <a name="create-resources-for-friendly-document-type-names"></a><span data-ttu-id="393fa-157">Crear recursos para nombres descriptivos de tipos de documentos</span><span class="sxs-lookup"><span data-stu-id="393fa-157">Create Resources for Friendly Document Type Names</span></span>

<span data-ttu-id="393fa-158">Debe implementar las cadenas de nombre descriptivo y de recuadro informativo para la aplicación como recursos de cadena.</span><span class="sxs-lookup"><span data-stu-id="393fa-158">You must implement friendly name and InfoTip strings for your application as string resources.</span></span> <span data-ttu-id="393fa-159">Para permitir que los nombres de tipo de documento descriptivos reaccionen al idioma de la interfaz de usuario, la aplicación debe registrar los nombres mediante el valor FriendlyTypeName bajo la clave de identificador de programa para el tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="393fa-159">To allow friendly document type names to react to the user interface language, the application must register the names using the FriendlyTypeName value under the program identifier key for the file type.</span></span> <span data-ttu-id="393fa-160">El valor predeterminado de la clave de identificador de programa debe conservarse para mantener la compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="393fa-160">The default value for the program identifier key should be retained to keep backward compatibility.</span></span> <span data-ttu-id="393fa-161">Para obtener información sobre cómo obtener acceso a los nombres de la aplicación, consulte los nombres de tipo de documento descriptivo de consulta en la sección registro de [Ubicación de cadenas redirigidas](locating-redirected-strings.md).</span><span class="sxs-lookup"><span data-stu-id="393fa-161">For information about accessing the names from your application, see the Query Friendly Document Type Names in the Registry section of [Locating Redirected Strings](locating-redirected-strings.md).</span></span>

<span data-ttu-id="393fa-162">El trabajo específico conlleva los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="393fa-162">The specific work involves the following steps:</span></span>

1.  <span data-ttu-id="393fa-163">Implemente el nombre descriptivo y las cadenas de recuadro como recursos de cadena específicos del lenguaje.</span><span class="sxs-lookup"><span data-stu-id="393fa-163">Implement the friendly name and InfoTip strings as language-specific string resources.</span></span>
2.  <span data-ttu-id="393fa-164">Agregue el valor FriendlyTypeName en la clave del registro de tipo de documento.</span><span class="sxs-lookup"><span data-stu-id="393fa-164">Add the FriendlyTypeName value under the document type registry key.</span></span> <span data-ttu-id="393fa-165">Los datos para el valor siguen el patrón " `@<path>,-<resID>` ", donde *rutaDeAcceso* indica el archivo ejecutable y *resID* es el identificador de recurso de un recurso de cadena localizable asociado a ese ejecutable.</span><span class="sxs-lookup"><span data-stu-id="393fa-165">The data for the value follows the pattern "`@<path>,-<resID>`", where *path* indicates the executable and *resID* is the resource identifier of a localizable string resource associated with that executable.</span></span>
3.  <span data-ttu-id="393fa-166">Especifique el valor del registro informativo según el formato " `@<path>,-<resID>` ".</span><span class="sxs-lookup"><span data-stu-id="393fa-166">Specify the InfoTip registry value according to the format "`@<path>,-<resID>`".</span></span>

<span data-ttu-id="393fa-167">En el ejemplo siguiente se muestra la configuración del registro de un archivo. txt:</span><span class="sxs-lookup"><span data-stu-id="393fa-167">The following example shows the registry settings for a .txt file:</span></span>


```C++
HKCR\.txt
@="txtfile"
"Content Type"="text/plain"

HKCR\txtfile
@="Text Document"

"FriendlyTypeName" = "@%systemroot%\system32\shell32.dll,-12345"

"InfoTip" = "@%systemroot%\system32\shell32.dll,-12346"
```



## <a name="provide-resources-for-shell-verb-action-strings"></a><span data-ttu-id="393fa-168">Proporcionar recursos para cadenas de acción de verbo de Shell</span><span class="sxs-lookup"><span data-stu-id="393fa-168">Provide Resources for Shell Verb Action Strings</span></span>

<span data-ttu-id="393fa-169">Las cadenas de acción para ciertos verbos, por ejemplo, "abrir" y "Editar", se muestran en el menú emergente que se muestra cuando el usuario hace clic con el botón secundario en un archivo en el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="393fa-169">Action strings for certain verbs, for example, "open" and "edit", are shown in the pop-up menu displayed when the user right-clicks a file in Windows Explorer.</span></span> <span data-ttu-id="393fa-170">La aplicación no tiene que especificar cadenas para los verbos de Shell comunes, ya que el shell tiene sus propios valores predeterminados habilitados para MUI para estos verbos.</span><span class="sxs-lookup"><span data-stu-id="393fa-170">Your application does not have to specify strings for common shell verbs, as the shell has its own MUI-enabled defaults for these verbs.</span></span> <span data-ttu-id="393fa-171">Sin embargo, debe proporcionar recursos de cadena localizable para las cadenas que representan verbos no comunes.</span><span class="sxs-lookup"><span data-stu-id="393fa-171">However, you should provide localizable string resources for strings representing uncommon verbs.</span></span>

<span data-ttu-id="393fa-172">En los sistemas operativos anteriores a Windows XP, las cadenas de verbos de Shell del registro se representan con la sintaxis siguiente, donde *Verb* especifica el nombre de verbo real:</span><span class="sxs-lookup"><span data-stu-id="393fa-172">On pre-Windows XP operating systems, strings for shell verbs in the registry are rendered using the following syntax, where *verb* specifies the actual verb name:</span></span>


```C++
HKCR\<progid>\shell\<verb>
@ = <friendly-name>
```



<span data-ttu-id="393fa-173">Este es un ejemplo:</span><span class="sxs-lookup"><span data-stu-id="393fa-173">Here's an example:</span></span>


```C++
HKCR\Sample.app\shell\Disc
@ = "Disconnect"
```



<span data-ttu-id="393fa-174">En Windows XP y versiones posteriores, puede usar un nivel de direccionamiento indirecto para que una cadena de acción dependa del idioma de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="393fa-174">On Windows XP and later, you can use a level of indirection to make an action string depend on user interface language.</span></span> <span data-ttu-id="393fa-175">Estos sistemas operativos admiten un valor MUIVerb para la definición de una cadena compatible con MUI.</span><span class="sxs-lookup"><span data-stu-id="393fa-175">These operating systems support a MUIVerb value for definition of a MUI-compatible string.</span></span> <span data-ttu-id="393fa-176">A continuación se muestra un ejemplo de una entrada del registro para un verbo no común:</span><span class="sxs-lookup"><span data-stu-id="393fa-176">Here's an example of a registry entry for an uncommon verb:</span></span>


```C++
HKCR\Sample.app\shell\Disc
@ = "Disconnect"
"MUIVerb" = "@%systemroot%\system32\sample.exe,-9875"
```



<span data-ttu-id="393fa-177">La aplicación MUI también debe poder registrar el valor predeterminado anterior como una cadena localizable, como se muestra a continuación:</span><span class="sxs-lookup"><span data-stu-id="393fa-177">Your MUI application should also be able to register the old default value as a localizable string, as shown below:</span></span>


```C++
HKCR\Sample.app\shell\Disc
@ = "@%systemroot%\system32\sample.exe,-9875"
```



> [!Note]  
> <span data-ttu-id="393fa-178">No se recomienda el registro del valor predeterminado anterior porque requiere una configuración diferente en Windows XP y versiones posteriores desde el programa de instalación usado en los sistemas operativos anteriores.</span><span class="sxs-lookup"><span data-stu-id="393fa-178">Registration of the old default value is not recommended because it requires a different setup on Windows XP and later from the setup used on earlier operating systems.</span></span>

 

## <a name="create-resources-for-verb-protocol-and-auxusertype-strings"></a><span data-ttu-id="393fa-179">Crear recursos para cadenas de verbo, protocolo y AuxUserType</span><span class="sxs-lookup"><span data-stu-id="393fa-179">Create Resources for Verb, Protocol, and AuxUserType Strings</span></span>

<span data-ttu-id="393fa-180">Debe crear recursos de cadena localizable para las cadenas de verbo, protocolo y AuxUserType.</span><span class="sxs-lookup"><span data-stu-id="393fa-180">You should create localizable string resources for Verb, Protocol, and AuxUserType strings.</span></span> <span data-ttu-id="393fa-181">Utilice la siguiente configuración del registro:</span><span class="sxs-lookup"><span data-stu-id="393fa-181">Use the following registry settings:</span></span>


```C++
HKCR\CLSID\{<Your_CLSID>}\Verb\<number> @="<Your Verb>, <menu_flag>, <verb_flag>"
"LocalizedString"="@<resDLLpath\resDLL.DLL>,-resStrID"
...

HKCR\CLSID\{<Your_CLSID>}\AuxUserType\<number>
@="<Your Short Name>"
"LocalizedString"="@<resDLLpath\resDLL.DLL>,-resStrID1"
...

HKCR\<Your_Name>\protocol\StdFileEditing\verb\<number>
@="<Your Verb>"
"LocalizedString"="@<resDLLpath\resDLL.DLL>,-resStrID"
...
```



<span data-ttu-id="393fa-182">El valor especificado para LocalizedString solo contiene o reemplaza el valor del *verbo*, no los dos valores de marca.</span><span class="sxs-lookup"><span data-stu-id="393fa-182">The value specified for LocalizedString only contains or replaces the value for *Your Verb*, not the two flag values.</span></span>

<span data-ttu-id="393fa-183">Este es un resumen para ayudarle a garantizar la correcta configuración del registro:</span><span class="sxs-lookup"><span data-stu-id="393fa-183">Here is a summary to help you ensure correct registry settings:</span></span>

-   <span data-ttu-id="393fa-184">Si CLSID tiene una clave que se va a \\ Insertar en el CLSID HKCR \\ {CLSID} \\ , defina el valor de CLSID predeterminado mediante HKCR \\ CLSID \\ {CLSID} \\ LocalizedString.</span><span class="sxs-lookup"><span data-stu-id="393fa-184">If CLSID has a HKCR\\CLSID\\{clsid}\\Insertable key, define the default CLSID value using HKCR\\CLSID\\{clsid}\\LocalizedString.</span></span>
-   <span data-ttu-id="393fa-185">Si CLSID tiene una o más subclaves en \\ el \\ verbo HKCR CLSID {CLSID} \\ , defina cada cadena de verbo individual mediante HKCR \\ CLSID \\ {CLSID} \\ verbo \\ XXX \\ LocalizedString.</span><span class="sxs-lookup"><span data-stu-id="393fa-185">If CLSID has one or more subkeys under HKCR\\CLSID\\{clsid}\\Verb, define each individual Verb string using HKCR\\CLSID\\{clsid}\\Verb\\xxx\\LocalizedString.</span></span>
-   <span data-ttu-id="393fa-186">Si CLSID tiene una o más subclaves en el \\ verbo HKCR {ProgID} \\ Protocol \\ Stdfileediting \\ , defina cada cadena de verbo individual mediante HKCR \\ {ProgID} \\ Protocol \\ Stdfileediting \\ verbo \\ XXX \\ LocalizedString.</span><span class="sxs-lookup"><span data-stu-id="393fa-186">If CLSID has one or more subkeys under HKCR\\{progid}\\Protocol\\Stdfileediting\\Verb, define each individual Verb string using HKCR\\{progid}\\Protocol\\Stdfileediting\\Verb\\xxx\\LocalizedString.</span></span>
-   <span data-ttu-id="393fa-187">Si CLSID tiene una o más subclaves de AuxUserType enumeradas en HKCR \\ CLSID \\ {CLSID} \\ AuxUserType, defina cada entrada de AuxUserType mediante HKCR \\ CLSID \\ {CLSID} \\ AuxUserType \\ XXX \\ LocalizedString.</span><span class="sxs-lookup"><span data-stu-id="393fa-187">If CLSID has one or more listed AuxUserType subkeys under HKCR\\CLSID\\{clsid}\\AuxUserType, define each AuxUserType entry using HKCR\\CLSID\\{clsid}\\AuxUserType\\xxx\\LocalizedString.</span></span>

## <a name="create-a-resource-for-the-uninstall-program"></a><span data-ttu-id="393fa-188">Crear un recurso para el programa de desinstalación</span><span class="sxs-lookup"><span data-stu-id="393fa-188">Create a Resource for the Uninstall Program</span></span>

<span data-ttu-id="393fa-189">Para registrar el programa de desinstalación de la aplicación, puede crear valores del registro en la subclave de identificador único de la aplicación en la clave del registro HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Uninstall.</span><span class="sxs-lookup"><span data-stu-id="393fa-189">To register the uninstall program for the application, you can create registry values in the unique identifier subkey for the application under the registry key HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows\\CurrentVersion\\Uninstall.</span></span> <span data-ttu-id="393fa-190">Entre los valores que se van a establecer se incluyen: DisplayName, DisplayVersion, Publisher, ProductID, RegOwner, RegCompany, UrlInfoAbout, HelpTelephone, HelpLink, InstallLocation, InstallSource, InstallDate, Contact, comments, DisplayIcon, README, UrlUpdateInfo.</span><span class="sxs-lookup"><span data-stu-id="393fa-190">Values to set include: DisplayName, DisplayVersion, Publisher, ProductID, RegOwner, RegCompany, UrlInfoAbout, HelpTelephone, HelpLink, InstallLocation, InstallSource, InstallDate, Contact, Comments, DisplayIcon, Readme, UrlUpdateInfo.</span></span>

> [!Note]  
> <span data-ttu-id="393fa-191">Para habilitar la tecnología MUI para cada valor, puede anexar " \_ adaptado" al nombre del valor.</span><span class="sxs-lookup"><span data-stu-id="393fa-191">To enable MUI technology for each value, you can append "\_Localized" to the value name.</span></span>

 

<span data-ttu-id="393fa-192">Los componentes del sistema operativo son necesarios para proporcionar un valor para DisplayName \_ adaptado en una forma específica de MUI.</span><span class="sxs-lookup"><span data-stu-id="393fa-192">Operating system components are required to provide a value for DisplayName\_Localized in a MUI-specific way.</span></span> <span data-ttu-id="393fa-193">Debe colocar el nombre para mostrar en un archivo DLL, como Res.dll, como un recurso de cadena, suponiendo que el identificador sea 1245.</span><span class="sxs-lookup"><span data-stu-id="393fa-193">You should place the display name in a DLL, such as Res.dll, as a string resource, assuming the identifier to be 1245.</span></span> <span data-ttu-id="393fa-194">A continuación, la aplicación puede registrar el nombre para mostrar como DisplayName \_ localizado con el valor "@ \\res.DLL,-1245".</span><span class="sxs-lookup"><span data-stu-id="393fa-194">Then the application can register the display name as DisplayName\_Localized with value "@\\res.DLL,-1245".</span></span> <span data-ttu-id="393fa-195">Todos los demás valores del registro deben conservarse tal como están, incluido el valor original de DisplayName.</span><span class="sxs-lookup"><span data-stu-id="393fa-195">All the other registry settings should be retained as they are, including the original value for DisplayName.</span></span>

## <a name="create-resources-for-sound-events"></a><span data-ttu-id="393fa-196">Crear recursos para eventos de sonido</span><span class="sxs-lookup"><span data-stu-id="393fa-196">Create Resources for Sound Events</span></span>

<span data-ttu-id="393fa-197">Windows asocia ciertos eventos con archivos de sonido, por ejemplo, un nuevo evento de notificación de correo o un evento de alarma de batería crítica.</span><span class="sxs-lookup"><span data-stu-id="393fa-197">Windows associates certain events with sound files, for example, a New Mail Notification event or a Critical Battery Alarm event.</span></span> <span data-ttu-id="393fa-198">Los nombres de evento deben mostrarse en la interfaz de usuario y deben admitir la globalización.</span><span class="sxs-lookup"><span data-stu-id="393fa-198">The event names must be displayed by the user interface and must support globalization.</span></span> <span data-ttu-id="393fa-199">Por lo tanto, debe implementar un recurso de cadena localizable para la descripción de cada descripción del evento.</span><span class="sxs-lookup"><span data-stu-id="393fa-199">Therefore, you should implement a localizable string resource for the description of each event description.</span></span> <span data-ttu-id="393fa-200">Agregue un nuevo valor del registro para cada nombre de evento, además del valor predeterminado codificado de forma rígida.</span><span class="sxs-lookup"><span data-stu-id="393fa-200">Add a new registry value for each event name, in addition to the hard-coded default value.</span></span>

<span data-ttu-id="393fa-201">Haga lo siguiente para habilitar un evento de sonido:</span><span class="sxs-lookup"><span data-stu-id="393fa-201">Do the following to enable a sound event:</span></span>

1.  <span data-ttu-id="393fa-202">Implemente la descripción como un recurso de cadena localizable.</span><span class="sxs-lookup"><span data-stu-id="393fa-202">Implement the description as a localizable string resource.</span></span>
2.  <span data-ttu-id="393fa-203">Agregue un nuevo valor del registro para el nombre para mostrar, además del valor predeterminado codificado de forma rígida.</span><span class="sxs-lookup"><span data-stu-id="393fa-203">Add a new registry value for the display name, in addition to the hard-coded default value.</span></span> <span data-ttu-id="393fa-204">A continuación se muestra el diseño del registro asociado:</span><span class="sxs-lookup"><span data-stu-id="393fa-204">The associated registry layout is shown below:</span></span>


```C++
HKCR\AppEvents\EventLabels
<event_name>
    (Default) REG_SZ "<description>"
    DispFileName REG_EXPAND_SZ "@<path>,-<resID>"
```



<span data-ttu-id="393fa-205">Si el shell no puede encontrar o recuperar el valor de DispFileName, utiliza la descripción predeterminada.</span><span class="sxs-lookup"><span data-stu-id="393fa-205">If the shell cannot find or retrieve the value of DispFileName, it uses the default description.</span></span>

## <a name="create-resources-for-keyboard-layout-strings"></a><span data-ttu-id="393fa-206">Crear recursos para cadenas de distribución de teclado</span><span class="sxs-lookup"><span data-stu-id="393fa-206">Create Resources for Keyboard Layout Strings</span></span>

<span data-ttu-id="393fa-207">Si la aplicación implementa una distribución del teclado, requiere un recurso de cadena localizable como nombre del diseño para la presentación en pantalla, por ejemplo, en las listas de distribuciones del teclado.</span><span class="sxs-lookup"><span data-stu-id="393fa-207">If your application implements a keyboard layout, it requires a localizable string resource for the name of the layout for screen display, for example, in lists of keyboard layouts.</span></span> <span data-ttu-id="393fa-208">Cada distribución del teclado tiene una clave del registro en HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ control \\ Keyboard Distributions.</span><span class="sxs-lookup"><span data-stu-id="393fa-208">Each keyboard layout has a registry key under HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\Keyboard Layouts.</span></span>

<span data-ttu-id="393fa-209">Entre los valores de esa clave están el texto de diseño, un nombre legible para la compatibilidad con versiones anteriores y el nombre para mostrar del diseño.</span><span class="sxs-lookup"><span data-stu-id="393fa-209">Among the values for that key are Layout Text, a human-readable name for backward compatibility, and Layout Display Name.</span></span> <span data-ttu-id="393fa-210">Los datos proporcionados para el nombre para mostrar del diseño deben ser una referencia de cadena con el formato " `@<path>,-resID` ", haciendo referencia a un recurso de cadena localizable asociado a la distribución del teclado.</span><span class="sxs-lookup"><span data-stu-id="393fa-210">The data supplied for Layout Display Name should be a string reference of the form "`@<path>,-resID`", referring to a localizable string resource associated with the keyboard layout.</span></span>

<span data-ttu-id="393fa-211">Este es un ejemplo de una configuración del registro para la distribución del teclado español (España):</span><span class="sxs-lookup"><span data-stu-id="393fa-211">Here is an example of a registry setting for the Spanish (Spain) keyboard layout:</span></span>

`Layout Display Name=@%SystemRoot%\system32\input.dll,-5020`

## <a name="represent-ole-insert-object-common-dialog-strings"></a><span data-ttu-id="393fa-212">Representar cadenas de cuadro de diálogo comunes de objetos Insert OLE</span><span class="sxs-lookup"><span data-stu-id="393fa-212">Represent OLE Insert Object Common Dialog Strings</span></span>

<span data-ttu-id="393fa-213">Puede implementar el nombre para mostrar de un objeto OLE insertable como un recurso de cadena localizable asociado al código que implementa dicho objeto.</span><span class="sxs-lookup"><span data-stu-id="393fa-213">You can implement the display name of an OLE insertable object as a localizable string resource associated with the code implementing that object.</span></span> <span data-ttu-id="393fa-214">El [cuadro de diálogo Insertar objeto OLE](/cpp/mfc/reference/coleinsertdialog-class) obtiene un nombre para mostrar de la clave del registro HKCR \\ CLSID \\ { *<GUID>* }, donde *GUID* identifica el identificador de clase de un objeto OLE insertable.</span><span class="sxs-lookup"><span data-stu-id="393fa-214">The [OLE Insert Object dialog box](/cpp/mfc/reference/coleinsertdialog-class) gets a display name from the registry key HKCR\\CLSID\\{*<GUID>*}, where *GUID* identifies the class identifier of an insertable OLE object.</span></span> <span data-ttu-id="393fa-215">Windows Vista y versiones posteriores implementan este tipo de objeto de forma localizable, utilizando un nombre para mostrar compatible con MUI que permite la personalización en el idioma de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="393fa-215">Windows Vista and later implement this type of object in a localizable way, using a MUI-compliant display name that allows customization to the user interface language.</span></span> <span data-ttu-id="393fa-216">En cambio, los sistemas operativos anteriores a Windows Vista implementan el nombre para mostrar de este tipo de objeto utilizando el valor predeterminado de la clave del registro correspondiente.</span><span class="sxs-lookup"><span data-stu-id="393fa-216">In contrast, pre-Windows Vista operating systems implement the display name for this type of object using the default value of the corresponding registry key.</span></span> <span data-ttu-id="393fa-217">Normalmente, este nombre es un nombre en inglés (Estados Unidos) o un nombre en el idioma de la interfaz de usuario predeterminada del sistema.</span><span class="sxs-lookup"><span data-stu-id="393fa-217">Typically this name is either an English (United States) name or a name in the system default UI language.</span></span>

> [!Note]  
> <span data-ttu-id="393fa-218">No se pueden insertar todos los objetos que corresponden a las subclaves de la clave del registro.</span><span class="sxs-lookup"><span data-stu-id="393fa-218">Not all objects that correspond to subkeys of the registry key are insertable.</span></span>

 

<span data-ttu-id="393fa-219">El valor predeterminado de la \\ clave HKCR CLSID \\ { *<GUID>* } debe conservar un nombre legible para la compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="393fa-219">The default value of the HKCR\\CLSID\\{*<GUID>*} key should retain a human-readable name for backward compatibility.</span></span> <span data-ttu-id="393fa-220">Sin embargo, también debe definir el valor de LocalizedString, con el formato " `@<path>,-ResID` ", donde ruta de acceso identifica el archivo ejecutable que implementa el objeto.</span><span class="sxs-lookup"><span data-stu-id="393fa-220">However, it should also define the LocalizedString value, in the format "`@<path>,-ResID`", where path identifies the executable file implementing the object.</span></span> <span data-ttu-id="393fa-221">El valor ResID especifica el identificador de recurso de la cadena localizable para el nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="393fa-221">The ResID value specifies the resource identifier of the localizable string for the display name.</span></span>

<span data-ttu-id="393fa-222">Por ejemplo, el script de registro para el objeto de clip multimedia insertable incluye las siguientes líneas:</span><span class="sxs-lookup"><span data-stu-id="393fa-222">For example, the registration script for the insertable Media Clip object includes the following lines:</span></span>


```C++
HKCR,"CLSID\%CLSID_Media_Clip%",,,"%default description%"
HKCR,"CLSID\%CLSID_Media_Clip%","LocalizedString",,"@%systemroot%\system32\mplay32.exe,-9217"
```



<span data-ttu-id="393fa-223">La primera línea proporciona compatibilidad con versiones anteriores colocando una cadena de texto simple en el registro como un nombre para mostrar predeterminado.</span><span class="sxs-lookup"><span data-stu-id="393fa-223">The first line provides backward compatibility by placing a simple text string in the registry as a default display name.</span></span> <span data-ttu-id="393fa-224">La segunda línea proporciona acceso al nombre para mostrar compatible con MUI.</span><span class="sxs-lookup"><span data-stu-id="393fa-224">The second line provides access to the MUI-compliant display name.</span></span> <span data-ttu-id="393fa-225">Indica el identificador de cadena almacenado en Mplay32.exe.</span><span class="sxs-lookup"><span data-stu-id="393fa-225">It indicates the string identifier stored in Mplay32.exe.</span></span> <span data-ttu-id="393fa-226">La cadena con el identificador 9217 en Mplay32.exe se puede asociar a valores de recursos de cadena para cualquier número de lenguajes.</span><span class="sxs-lookup"><span data-stu-id="393fa-226">The string with identifier 9217 in Mplay32.exe can be associated with string resource values for any number of languages.</span></span> <span data-ttu-id="393fa-227">Su nombre en inglés (Estados Unidos) es "clip multimedia".</span><span class="sxs-lookup"><span data-stu-id="393fa-227">Its English (United States) name is "Media Clip".</span></span>

## <a name="create-string-resources-for-microsoft-management-console-snap-ins"></a><span data-ttu-id="393fa-228">Crear recursos de cadena para Microsoft Management Console Snap-Ins</span><span class="sxs-lookup"><span data-stu-id="393fa-228">Create String Resources for Microsoft Management Console Snap-Ins</span></span>

<span data-ttu-id="393fa-229">Debe crear un recurso de cadena localizable para cada complemento de Microsoft Management Console (MMC) que usa la aplicación de MUI.</span><span class="sxs-lookup"><span data-stu-id="393fa-229">You should create a localizable string resource for each Microsoft Management Console (MMC) snap-in used by your MUI application.</span></span> <span data-ttu-id="393fa-230">Dado que un complemento es parte de una consola, tiene una interfaz de usuario y debe globalizarse para funcionar en más de un idioma.</span><span class="sxs-lookup"><span data-stu-id="393fa-230">Because a snap-in is part of a console, it has a user interface and must be globalized to operate in more than one language.</span></span>

<span data-ttu-id="393fa-231">En su mayor parte, los complementos MMC producen los mismos problemas de globalización y localización que la propia aplicación de MUI.</span><span class="sxs-lookup"><span data-stu-id="393fa-231">For the most part, MMC snap-ins raise the same globalization and localization issues as the MUI application itself.</span></span> <span data-ttu-id="393fa-232">Un complemento MMC debe reflejar su nombre en el registro para mostrarlo.</span><span class="sxs-lookup"><span data-stu-id="393fa-232">An MMC snap-in must reflect its name in the registry for display.</span></span> <span data-ttu-id="393fa-233">La entrada del registro debe incluir una referencia indirecta a un recurso de cadena localizable y una cadena literal para mantener la compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="393fa-233">The registry entry should include both an indirect reference to a localizable string resource and a literal string for backward compatibility.</span></span>

<span data-ttu-id="393fa-234">Cada complemento MMC tiene una clave del registro en HKEY \_ local \_ Machine \\ software \\ Microsoft \\ MMC \\ complementos.</span><span class="sxs-lookup"><span data-stu-id="393fa-234">Each MMC snap-in has a registry key under HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\MMC\\SnapIns.</span></span> <span data-ttu-id="393fa-235">Entre los valores de esa clave se NameString, especificando un nombre legible para la compatibilidad con versiones anteriores y NameStringIndirect, especificando una referencia indirecta a un recurso de cadena localizable.</span><span class="sxs-lookup"><span data-stu-id="393fa-235">Among the values for that key are NameString, specifying a human-readable name for backward compatibility, and NameStringIndirect, specifying an indirect reference to a localizable string resource.</span></span> <span data-ttu-id="393fa-236">En el caso de NameStringIndirect, debe proporcionar una referencia de cadena con el formato " `@<path>,-resID` ", que representa un recurso de cadena localizable.</span><span class="sxs-lookup"><span data-stu-id="393fa-236">For NameStringIndirect, you should provide a string reference of the form "`@<path>,-resID`", representing a localizable string resource.</span></span>

<span data-ttu-id="393fa-237">Por ejemplo, puede establecer la siguiente configuración para Mymmc.dll, donde 12345 es el identificador del recurso de cadena correspondiente que contiene el nombre traducible del complemento:</span><span class="sxs-lookup"><span data-stu-id="393fa-237">For example, you might make the following setting for Mymmc.dll, where 12345 is the identifier of the corresponding string resource containing the localizable name of the snap-in:</span></span>


```C++
NameStringIndirect=@%systemroot%@c:\windir\system32\mymmc.dll,-12345
```



<span data-ttu-id="393fa-238">Algunos complementos registran otros valores de cadena del registro que MMC no lee del registro.</span><span class="sxs-lookup"><span data-stu-id="393fa-238">Some snap-ins register other registry string values that MMC does not read from the registry.</span></span> <span data-ttu-id="393fa-239">Para obtener más información sobre el uso de estos valores, consulte registrar Microsoft Management Console Snap-In cadenas no leídas del registro en [localizar cadenas redirigidas](locating-redirected-strings.md).</span><span class="sxs-lookup"><span data-stu-id="393fa-239">For more information about using these values, see Register Microsoft Management Console Snap-In Strings Not Read from the Registry in [Locating Redirected Strings](locating-redirected-strings.md).</span></span>

## <a name="create-string-resources-for-a-windows-service"></a><span data-ttu-id="393fa-240">Crear recursos de cadena para un servicio de Windows</span><span class="sxs-lookup"><span data-stu-id="393fa-240">Create String Resources for a Windows Service</span></span>

<span data-ttu-id="393fa-241">Aunque un servicio de Windows normalmente tiene poca o ninguna interfaz de usuario, debe mostrar un nombre compatible con MUI y, normalmente, proporciona una descripción específica del lenguaje compatible con MUI.</span><span class="sxs-lookup"><span data-stu-id="393fa-241">Although a Windows service typically has little or no user interface, it must display a MUI-compliant name and usually provides a MUI-compliant language-specific description.</span></span> <span data-ttu-id="393fa-242">La clave del registro que describe un servicio de Windows solo admite el valor DisplayName para el nombre del servicio y el valor de descripción de la descripción del servicio.</span><span class="sxs-lookup"><span data-stu-id="393fa-242">The registry key that describes a Windows service supports only the DisplayName value for the service name and the Description value for the service description.</span></span>

<span data-ttu-id="393fa-243">La configuración del servicio de Windows se realiza desde la aplicación, tal y como se describe en establecer el nombre para mostrar y la descripción de un servicio de Windows desde el registro en [localizar cadenas redirigidas](locating-redirected-strings.md).</span><span class="sxs-lookup"><span data-stu-id="393fa-243">Settings for the Windows service are made from the application, as described in Set the Display Name and Description for a Windows Service from the Registry in [Locating Redirected Strings](locating-redirected-strings.md).</span></span> <span data-ttu-id="393fa-244">Si la aplicación no establece los valores del registro para la interfaz de usuario del servicio, los valores del registro permanecen establecidos en inglés, aunque la interfaz de usuario esté en otro idioma.</span><span class="sxs-lookup"><span data-stu-id="393fa-244">If your application does not set the registry values for the service user interface, values in the registry remain set to English, even if the user interface is in another language.</span></span>

## <a name="related-topics"></a><span data-ttu-id="393fa-245">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="393fa-245">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="393fa-246">Preparación de recursos</span><span class="sxs-lookup"><span data-stu-id="393fa-246">Preparing Resources</span></span>](preparing-resources.md)
</dt> <dt>

[<span data-ttu-id="393fa-247">Localizar cadenas redirigidas</span><span class="sxs-lookup"><span data-stu-id="393fa-247">Locating Redirected Strings</span></span>](locating-redirected-strings.md)
</dt> </dl>

 

 
