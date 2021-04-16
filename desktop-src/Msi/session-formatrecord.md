---
description: El método FormatRecord del objeto de sesión devuelve una cadena con formato a partir de una plantilla y datos de registro.
ms.assetid: 2018ac75-ea18-4256-8d56-0527069ce24b
title: Método Session. FormatRecord
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FormatRecord
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e87c73e5ef7adafd9caab00bf257fe8a7afc3c33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679518"
---
# <a name="sessionformatrecord-method"></a><span data-ttu-id="9eb53-103">Método Session. FormatRecord</span><span class="sxs-lookup"><span data-stu-id="9eb53-103">Session.FormatRecord method</span></span>

<span data-ttu-id="9eb53-104">El método **FormatRecord** del objeto de [**sesión**](session-object.md) devuelve una cadena con formato a partir de una plantilla y datos de registro.</span><span class="sxs-lookup"><span data-stu-id="9eb53-104">The **FormatRecord** method of the [**Session**](session-object.md) object returns a formatted string from a template and record data.</span></span>

## <a name="syntax"></a><span data-ttu-id="9eb53-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9eb53-105">Syntax</span></span>


```JScript
Session.FormatRecord(
  record
)
```



## <a name="parameters"></a><span data-ttu-id="9eb53-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9eb53-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9eb53-107">*record*</span><span class="sxs-lookup"><span data-stu-id="9eb53-107">*record*</span></span> 
</dt> <dd>

<span data-ttu-id="9eb53-108">Objeto de **registro** necesario que contiene una plantilla y los datos a los que se va a dar formato.</span><span class="sxs-lookup"><span data-stu-id="9eb53-108">Required **Record** object containing a template and data to be formatted.</span></span> <span data-ttu-id="9eb53-109">La cadena de plantilla debe establecerse en el campo 0 seguido de los parámetros de datos a los que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="9eb53-109">The template string must be set in field 0 followed by any referenced data parameters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9eb53-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9eb53-110">Return value</span></span>

<span data-ttu-id="9eb53-111">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="9eb53-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9eb53-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9eb53-112">Remarks</span></span>

<span data-ttu-id="9eb53-113">El método **FormatRecord** usa el siguiente proceso de formato.</span><span class="sxs-lookup"><span data-stu-id="9eb53-113">The **FormatRecord** method uses the following format process.</span></span>

<span data-ttu-id="9eb53-114">Los parámetros a los que se va a [dar formato](formatted.md) se incluyen entre corchetes \[ .. \] .</span><span class="sxs-lookup"><span data-stu-id="9eb53-114">Parameters to be [formatted](formatted.md) are enclosed in square brackets \[..\].</span></span> <span data-ttu-id="9eb53-115">Los corchetes se pueden recorrer en iteración porque las sustituciones se resuelven desde fuera.</span><span class="sxs-lookup"><span data-stu-id="9eb53-115">The square brackets can be iterated because the substitutions are resolved from inside out.</span></span>

<span data-ttu-id="9eb53-116">Si una parte de la cadena está entre llaves {} y no contiene corchetes, la parte se deja sin cambios, incluidas las llaves.</span><span class="sxs-lookup"><span data-stu-id="9eb53-116">If a part of the string is enclosed in curly braces { } and contains no square brackets, the part is left unchanged, including the curly braces.</span></span>

<span data-ttu-id="9eb53-117">Si una parte de la cadena está entre llaves y contiene uno o varios nombres de propiedad y, si se encuentran todas las propiedades, el texto (con las sustituciones resueltas) se muestra sin las llaves.</span><span class="sxs-lookup"><span data-stu-id="9eb53-117">If a part of the string is enclosed in curly braces and contains one or more property names, and if all the properties are found, the text (with the resolved substitutions) is displayed without the curly braces.</span></span> <span data-ttu-id="9eb53-118">Si no se encuentra ninguna de las propiedades, se quitarán todo el texto de las llaves y las llaves.</span><span class="sxs-lookup"><span data-stu-id="9eb53-118">If any of the properties are not found, all the text in the curly braces and the braces themselves are removed.</span></span>

<span data-ttu-id="9eb53-119">**Para dar formato a cadenas mediante el método FormatRecord**</span><span class="sxs-lookup"><span data-stu-id="9eb53-119">**To format strings using the FormatRecord method**</span></span>

1.  <span data-ttu-id="9eb53-120">Los parámetros numéricos se sustituyen sustituyendo el marcador por el valor del campo registro correspondiente, con los valores que faltan o null no generan texto.</span><span class="sxs-lookup"><span data-stu-id="9eb53-120">The numeric parameters are substituted by replacing the marker with the value of the corresponding record field, with missing or Null values producing no text.</span></span>
2.  <span data-ttu-id="9eb53-121">La cadena resultante se procesa reemplazando los parámetros que no son de registro por los valores correspondientes, como se indica en las siguientes descripciones.</span><span class="sxs-lookup"><span data-stu-id="9eb53-121">The string that results is processed by replacing the non-record parameters with the corresponding values, as noted in the following descriptions.</span></span>
    -   <span data-ttu-id="9eb53-122">Si se encuentra una subcadena con el formato " \[ PropertyName \] ", se reemplaza por el valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="9eb53-122">If a substring of the form "\[propertyname\]" is encountered, it is replaced by the value of the property.</span></span>
    -   <span data-ttu-id="9eb53-123">Si se encuentra una subcadena con el formato " \[ % environmentvariable \] ", se sustituye el valor de la variable de entorno.</span><span class="sxs-lookup"><span data-stu-id="9eb53-123">If a substring of the form "\[%environmentvariable\]" is found, the value of the environment variable is substituted.</span></span>
    -   <span data-ttu-id="9eb53-124">Si se encuentra una subcadena con el formato \[ \# *filekey* \] , se reemplaza por la ruta de acceso completa del archivo, con el valor *filekey* usado como clave en la [tabla de archivos](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="9eb53-124">If a substring of the form \[\#*filekey*\] is found, it is replaced by the full path of the file, with the value *filekey* used as a key into the [File table](file-table.md).</span></span> <span data-ttu-id="9eb53-125">El valor de \[ \# *filekey* \] permanece en blanco y no se reemplaza por una ruta de acceso hasta que el instalador ejecuta la acción [CostInitialize](costinitialize-action.md), la acción [FileCost](filecost-action.md)y la [acción CostFinalize](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="9eb53-125">The value of \[\#*filekey*\] remains blank and is not replaced by a path until the installer runs the [CostInitialize action](costinitialize-action.md), [FileCost action](filecost-action.md), and [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="9eb53-126">El valor de \[ \# *filekey* \] depende del estado de instalación del componente al que pertenece el archivo.</span><span class="sxs-lookup"><span data-stu-id="9eb53-126">The value of \[\#*filekey*\] depends upon the installation state of the component to which the file belongs.</span></span> <span data-ttu-id="9eb53-127">Si el componente se ejecuta desde el origen, el valor es la ruta de acceso a la ubicación de origen del archivo.</span><span class="sxs-lookup"><span data-stu-id="9eb53-127">If the component is being run from source, the value is the path to the source location of the file.</span></span> <span data-ttu-id="9eb53-128">Si el componente se ejecuta localmente, el valor es la ruta de acceso a la ubicación de destino del archivo después de la instalación.</span><span class="sxs-lookup"><span data-stu-id="9eb53-128">If the component is being run locally, the value is the path to the target location of the file after installation.</span></span> <span data-ttu-id="9eb53-129">Si el componente no está presente, la ruta de acceso está en blanco.</span><span class="sxs-lookup"><span data-stu-id="9eb53-129">If the component is absent, the path is blank.</span></span> <span data-ttu-id="9eb53-130">Para obtener más información acerca de cómo comprobar el estado de instalación de los componentes de, vea [comprobar la instalación de características, componentes y archivos](checking-the-installation-of-features-components-files.md).</span><span class="sxs-lookup"><span data-stu-id="9eb53-130">For more information about checking the installation state of components, see [Checking the Installation of Features, Components, Files](checking-the-installation-of-features-components-files.md).</span></span>
    -   <span data-ttu-id="9eb53-131">Si se encuentra una subcadena con el formato \[ *$componentkey* \] , se reemplaza por el directorio de instalación del componente, con el valor *componentkey* usado como clave en la tabla de [componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="9eb53-131">If a substring of the form \[*$componentkey*\] is found, it is replaced by the install directory of the component, with the value *componentkey* used as a key into the [Component table](component-table.md).</span></span> <span data-ttu-id="9eb53-132">El valor de \[ $ *componentkey* \] permanece en blanco y no se reemplaza por un directorio hasta que el instalador ejecuta la acción [CostInitialize](costinitialize-action.md), la acción [FileCost](filecost-action.md)y la [acción CostFinalize](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="9eb53-132">The value of \[$*componentkey*\] remains blank and is not replaced by a directory until the installer runs the [CostInitialize action](costinitialize-action.md), [FileCost action](filecost-action.md), and [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="9eb53-133">El valor de \[ $ *componentkey* \] depende del estado de la instalación del componente.</span><span class="sxs-lookup"><span data-stu-id="9eb53-133">The value of \[$*componentkey*\] depends upon the installation state of the component.</span></span> <span data-ttu-id="9eb53-134">Si el componente se ejecuta desde el origen, el valor es el directorio de origen del archivo.</span><span class="sxs-lookup"><span data-stu-id="9eb53-134">If the component is being run from source, the value is the source directory of the file.</span></span> <span data-ttu-id="9eb53-135">Si el componente se ejecuta localmente, el valor es el directorio de destino después de la instalación.</span><span class="sxs-lookup"><span data-stu-id="9eb53-135">If the component is being run locally, the value is the target directory after installation.</span></span> <span data-ttu-id="9eb53-136">Si el componente está ausente, el valor se deja en blanco.</span><span class="sxs-lookup"><span data-stu-id="9eb53-136">If the component is absent, the value is left blank.</span></span> <span data-ttu-id="9eb53-137">Para obtener más información acerca de cómo comprobar el estado de instalación de los componentes de, vea [comprobar la instalación de características, componentes y archivos](checking-the-installation-of-features-components-files.md).</span><span class="sxs-lookup"><span data-stu-id="9eb53-137">For more information about checking the installation state of components, see [Checking the Installation of Features, Components, Files](checking-the-installation-of-features-components-files.md).</span></span>
    -   <span data-ttu-id="9eb53-138">Si se encuentra una subcadena con el formato " \[ \\ c \] ", se reemplaza por el carácter sin ningún procesamiento adicional.</span><span class="sxs-lookup"><span data-stu-id="9eb53-138">If a substring of the form "\[\\c\]" is found, it is replaced by the character without any further processing.</span></span> <span data-ttu-id="9eb53-139">Solo se mantiene el primer carácter después de la barra diagonal inversa; se quita todo lo demás.</span><span class="sxs-lookup"><span data-stu-id="9eb53-139">Only the first character after the backslash is kept; everything else is removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="9eb53-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9eb53-140">Requirements</span></span>



| <span data-ttu-id="9eb53-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="9eb53-141">Requirement</span></span> | <span data-ttu-id="9eb53-142">Value</span><span class="sxs-lookup"><span data-stu-id="9eb53-142">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9eb53-143">Versión</span><span class="sxs-lookup"><span data-stu-id="9eb53-143">Version</span></span><br/> | <span data-ttu-id="9eb53-144">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9eb53-144">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="9eb53-145">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9eb53-145">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="9eb53-146">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="9eb53-146">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="9eb53-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9eb53-147">DLL</span></span><br/>     | <dl> <span data-ttu-id="9eb53-148"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9eb53-148"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="9eb53-149">IID</span><span class="sxs-lookup"><span data-stu-id="9eb53-149">IID</span></span><br/>     | <span data-ttu-id="9eb53-150">El IID \_ ISession se define como 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="9eb53-150">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



## <a name="see-also"></a><span data-ttu-id="9eb53-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="9eb53-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9eb53-152">Formatea</span><span class="sxs-lookup"><span data-stu-id="9eb53-152">Formatted</span></span>](formatted.md)
</dt> <dt>

[<span data-ttu-id="9eb53-153">Tipos de datos de columna</span><span class="sxs-lookup"><span data-stu-id="9eb53-153">Column Data Types</span></span>](column-data-types.md)
</dt> </dl>

 

 




