---
title: Mensaje de LB_DIR (Winuser. h)
description: Agrega nombres a la lista mostrada por un cuadro de lista. El mensaje agrega los nombres de los directorios y archivos que coinciden con una cadena y un conjunto de atributos de archivo especificados. LB \_ dir también puede Agregar Letras de unidad asignadas al cuadro de lista.
ms.assetid: 5ec134e9-fe42-4cc0-bdea-fa5e66c218f6
keywords:
- LB_DIR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_DIR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80abddbce13adec2e66824057fc5e873def306ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151059"
---
# <a name="lb_dir-message"></a><span data-ttu-id="2cad1-106">Mensaje de LB \_ dir</span><span class="sxs-lookup"><span data-stu-id="2cad1-106">LB\_DIR message</span></span>

<span data-ttu-id="2cad1-107">Agrega nombres a la lista mostrada por un cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="2cad1-107">Adds names to the list displayed by a list box.</span></span> <span data-ttu-id="2cad1-108">El mensaje agrega los nombres de los directorios y archivos que coinciden con una cadena y un conjunto de atributos de archivo especificados.</span><span class="sxs-lookup"><span data-stu-id="2cad1-108">The message adds the names of directories and files that match a specified string and set of file attributes.</span></span> <span data-ttu-id="2cad1-109">**Lb \_ DIR** también puede Agregar Letras de unidad asignadas al cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="2cad1-109">**LB\_DIR** can also add mapped drive letters to the list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="2cad1-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2cad1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cad1-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2cad1-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2cad1-112">Atributos de los archivos o directorios que se van a agregar al cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="2cad1-112">The attributes of the files or directories to be added to the list box.</span></span> <span data-ttu-id="2cad1-113">Este parámetro puede ser uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="2cad1-113">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="2cad1-114">Value</span><span class="sxs-lookup"><span data-stu-id="2cad1-114">Value</span></span>                                                                                                                                                         | <span data-ttu-id="2cad1-115">Significado</span><span class="sxs-lookup"><span data-stu-id="2cad1-115">Meaning</span></span>                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DDL_ARCHIVE"></span><span id="ddl_archive"></span><dl> <span data-ttu-id="2cad1-116"><dt>**\_archivo DDL**</dt></span><span class="sxs-lookup"><span data-stu-id="2cad1-116"><dt>**DDL\_ARCHIVE**</dt></span></span> </dl>       | <span data-ttu-id="2cad1-117">Incluye archivos archivados.</span><span class="sxs-lookup"><span data-stu-id="2cad1-117">Includes archived files.</span></span><br/>                                                                                                            |
| <span id="DDL_DIRECTORY"></span><span id="ddl_directory"></span><dl> <span data-ttu-id="2cad1-118"><dt>**\_directorio DDL**</dt></span><span class="sxs-lookup"><span data-stu-id="2cad1-118"><dt>**DDL\_DIRECTORY**</dt></span></span> </dl> | <span data-ttu-id="2cad1-119">Incluye subdirectorios.</span><span class="sxs-lookup"><span data-stu-id="2cad1-119">Includes subdirectories.</span></span> <span data-ttu-id="2cad1-120">Los nombres de subdirectorios se incluyen entre corchetes ( \[ \] ).</span><span class="sxs-lookup"><span data-stu-id="2cad1-120">Subdirectory names are enclosed in square brackets (\[ \]).</span></span><br/>                                                |
| <span id="DDL_DRIVES"></span><span id="ddl_drives"></span><dl> <span data-ttu-id="2cad1-121"><dt>**\_unidades DDL**</dt></span><span class="sxs-lookup"><span data-stu-id="2cad1-121"><dt>**DDL\_DRIVES**</dt></span></span> </dl>          | <span data-ttu-id="2cad1-122">Todas las unidades asignadas se agregan a la lista.</span><span class="sxs-lookup"><span data-stu-id="2cad1-122">All mapped drives are added to the list.</span></span> <span data-ttu-id="2cad1-123">Las unidades se muestran en el formato \[ - *x* - \] , donde *x* es la letra de la unidad.</span><span class="sxs-lookup"><span data-stu-id="2cad1-123">Drives are listed in the form \[-*x*-\], where *x* is the drive letter.</span></span><br/>                    |
| <span id="DDL_EXCLUSIVE"></span><span id="ddl_exclusive"></span><dl> <span data-ttu-id="2cad1-124"><dt>**DDL \_ exclusivo**</dt></span><span class="sxs-lookup"><span data-stu-id="2cad1-124"><dt>**DDL\_EXCLUSIVE**</dt></span></span> </dl> | <span data-ttu-id="2cad1-125">Incluye solo los archivos con los atributos especificados.</span><span class="sxs-lookup"><span data-stu-id="2cad1-125">Includes only files with the specified attributes.</span></span> <span data-ttu-id="2cad1-126">De forma predeterminada, los archivos de lectura y escritura se enumeran incluso si \_ no se especifica DDL ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="2cad1-126">By default, read/write files are listed even if DDL\_READWRITE is not specified.</span></span><br/> |
| <span id="DDL_HIDDEN"></span><span id="ddl_hidden"></span><dl> <span data-ttu-id="2cad1-127"><dt>**DDL \_ oculto**</dt></span><span class="sxs-lookup"><span data-stu-id="2cad1-127"><dt>**DDL\_HIDDEN**</dt></span></span> </dl>          | <span data-ttu-id="2cad1-128">Incluye archivos ocultos.</span><span class="sxs-lookup"><span data-stu-id="2cad1-128">Includes hidden files.</span></span><br/>                                                                                                              |
| <span id="DDL_READONLY"></span><span id="ddl_readonly"></span><dl> <span data-ttu-id="2cad1-129"><dt>**DDL de \_ solo lectura**</dt></span><span class="sxs-lookup"><span data-stu-id="2cad1-129"><dt>**DDL\_READONLY**</dt></span></span> </dl>    | <span data-ttu-id="2cad1-130">Incluye archivos de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2cad1-130">Includes read-only files.</span></span><br/>                                                                                                           |
| <span id="DDL_READWRITE"></span><span id="ddl_readwrite"></span><dl> <span data-ttu-id="2cad1-131"><dt>**ReadWrite de DDL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2cad1-131"><dt>**DDL\_READWRITE**</dt></span></span> </dl> | <span data-ttu-id="2cad1-132">Incluye archivos de lectura/escritura sin atributos adicionales.</span><span class="sxs-lookup"><span data-stu-id="2cad1-132">Includes read/write files with no additional attributes.</span></span> <span data-ttu-id="2cad1-133">Esta es la configuración predeterminada.</span><span class="sxs-lookup"><span data-stu-id="2cad1-133">This is the default setting.</span></span><br/>                                               |
| <span id="DDL_SYSTEM"></span><span id="ddl_system"></span><dl> <span data-ttu-id="2cad1-134"><dt>**\_sistema DDL**</dt></span><span class="sxs-lookup"><span data-stu-id="2cad1-134"><dt>**DDL\_SYSTEM**</dt></span></span> </dl>          | <span data-ttu-id="2cad1-135">Incluye archivos del sistema.</span><span class="sxs-lookup"><span data-stu-id="2cad1-135">Includes system files.</span></span><br/>                                                                                                              |



 

</dd> <dt>

<span data-ttu-id="2cad1-136">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2cad1-136">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2cad1-137">Puntero a la cadena terminada en null que especifica una ruta de acceso absoluta, una ruta de acceso relativa o un nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="2cad1-137">A pointer to the null-terminated string that specifies an absolute path, relative path, or filename.</span></span> <span data-ttu-id="2cad1-138">Una ruta de acceso absoluta puede empezar con una letra de unidad (por ejemplo, d: \) o un nombre UNC (por ejemplo, \\ \\ *MachineName* \\ *ShareName*).</span><span class="sxs-lookup"><span data-stu-id="2cad1-138">An absolute path can begin with a drive letter (for example, d:\) or a UNC name (for example, \\\\ *machinename*\\ *sharename*).</span></span>

<span data-ttu-id="2cad1-139">Si la cadena especifica un nombre de archivo o directorio que tiene los atributos especificados por el parámetro *wParam* , el nombre de archivo o directorio se agrega a la lista.</span><span class="sxs-lookup"><span data-stu-id="2cad1-139">If the string specifies a filename or directory that has the attributes specified by the *wParam* parameter, the filename or directory is added to the list.</span></span> <span data-ttu-id="2cad1-140">Si el nombre de archivo o de directorio contiene caracteres comodín (?</span><span class="sxs-lookup"><span data-stu-id="2cad1-140">If the filename or directory name contains wildcard characters (?</span></span> <span data-ttu-id="2cad1-141">o \* ), todos los archivos o directorios que coinciden con la expresión comodín y que tienen los atributos especificados por el parámetro *wParam* se agregan a la lista.</span><span class="sxs-lookup"><span data-stu-id="2cad1-141">or \*), all files or directories that match the wildcard expression and have the attributes specified by the *wParam* parameter are added to the list.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2cad1-142">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2cad1-142">Return value</span></span>

<span data-ttu-id="2cad1-143">Si el mensaje se realiza correctamente, el valor devuelto es el índice de base cero del último nombre agregado a la lista.</span><span class="sxs-lookup"><span data-stu-id="2cad1-143">If the message succeeds, the return value is the zero-based index of the last name added to the list.</span></span>

<span data-ttu-id="2cad1-144">Si se produce un error, el valor devuelto es LB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="2cad1-144">If an error occurs, the return value is LB\_ERR.</span></span> <span data-ttu-id="2cad1-145">Si no hay suficiente espacio para almacenar las nuevas cadenas, el valor devuelto es LB \_ ERRSPACE.</span><span class="sxs-lookup"><span data-stu-id="2cad1-145">If there is insufficient space to store the new strings, the return value is LB\_ERRSPACE.</span></span>

## <a name="remarks"></a><span data-ttu-id="2cad1-146">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2cad1-146">Remarks</span></span>

<span data-ttu-id="2cad1-147">El mensaje [**lb \_ INITSTORAGE**](lb-initstorage.md) ayuda a acelerar la inicialización de cuadros de lista que tienen un gran número de elementos (más de 100).</span><span class="sxs-lookup"><span data-stu-id="2cad1-147">The [**LB\_INITSTORAGE**](lb-initstorage.md) message helps speed up the initialization of list boxes that have a large number of items (more than 100).</span></span> <span data-ttu-id="2cad1-148">Reserva la cantidad de memoria especificada para que los mensajes de **lb \_ dir** posteriores tarden el menor tiempo posible.</span><span class="sxs-lookup"><span data-stu-id="2cad1-148">It reserves the specified amount of memory so that subsequent **LB\_DIR** messages take the shortest possible time.</span></span> <span data-ttu-id="2cad1-149">Puede usar estimaciones para los parámetros *wParam* e *lParam* .</span><span class="sxs-lookup"><span data-stu-id="2cad1-149">You can use estimates for the *wParam* and *lParam* parameters.</span></span> <span data-ttu-id="2cad1-150">Si sobrestima, se asigna la memoria adicional; Si se subestima, se usa la asignación normal para los elementos que superan la cantidad solicitada.</span><span class="sxs-lookup"><span data-stu-id="2cad1-150">If you overestimate, the extra memory is allocated; if you underestimate, the normal allocation is used for items that exceed the requested amount.</span></span>

<span data-ttu-id="2cad1-151">Si *wParam* incluye la \_ marca de directorio DDL y *lParam* especifica todos los subdirectorios de un directorio de primer nivel, como C: \\ temp \\ \* , el cuadro de lista incluirá siempre una entrada ".." para el directorio raíz.</span><span class="sxs-lookup"><span data-stu-id="2cad1-151">If *wParam* includes the DDL\_DIRECTORY flag and *lParam* specifies all the subdirectories of a first-level directory, such as C:\\TEMP\\\*, the list box will always include a ".." entry for the root directory.</span></span> <span data-ttu-id="2cad1-152">Esto es así incluso si el directorio raíz tiene atributos ocultos o del sistema, y \_ \_ no se especifican las marcas DDL ocultas y del sistema DDL.</span><span class="sxs-lookup"><span data-stu-id="2cad1-152">This is true even if the root directory has hidden or system attributes and the DDL\_HIDDEN and DDL\_SYSTEM flags are not specified.</span></span> <span data-ttu-id="2cad1-153">El directorio raíz de un volumen NTFS tiene atributos ocultos y del sistema.</span><span class="sxs-lookup"><span data-stu-id="2cad1-153">The root directory of an NTFS volume has hidden and system attributes.</span></span>

<span data-ttu-id="2cad1-154">La lista muestra los nombres de archivo largos, si los hay.</span><span class="sxs-lookup"><span data-stu-id="2cad1-154">The list displays long filenames, if any.</span></span>

<span data-ttu-id="2cad1-155">En el caso de una aplicación ANSI, el sistema convierte el texto de un cuadro de lista en Unicode mediante CP \_ ACP.</span><span class="sxs-lookup"><span data-stu-id="2cad1-155">For an ANSI application, the system converts the text in a list box to Unicode using CP\_ACP.</span></span> <span data-ttu-id="2cad1-156">Esto puede causar problemas.</span><span class="sxs-lookup"><span data-stu-id="2cad1-156">This can cause problems.</span></span> <span data-ttu-id="2cad1-157">Por ejemplo, los caracteres romanos acentuados en un cuadro de lista no Unicode en las ventanas japonesas se desactivarán.</span><span class="sxs-lookup"><span data-stu-id="2cad1-157">For example, accented Roman characters in a non-Unicode list box in Japanese Windows will come out garbled.</span></span> <span data-ttu-id="2cad1-158">Para solucionar este error, compile la aplicación como Unicode o use un cuadro de lista dibujado por el propietario.</span><span class="sxs-lookup"><span data-stu-id="2cad1-158">To fix this, either compile the application as Unicode or use an owner-drawn list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="2cad1-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2cad1-159">Requirements</span></span>



| <span data-ttu-id="2cad1-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="2cad1-160">Requirement</span></span> | <span data-ttu-id="2cad1-161">Value</span><span class="sxs-lookup"><span data-stu-id="2cad1-161">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cad1-162">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2cad1-162">Minimum supported client</span></span><br/> | <span data-ttu-id="2cad1-163">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2cad1-163">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2cad1-164">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2cad1-164">Minimum supported server</span></span><br/> | <span data-ttu-id="2cad1-165">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="2cad1-165">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2cad1-166">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2cad1-166">Header</span></span><br/>                   | <dl> <span data-ttu-id="2cad1-167"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2cad1-167"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2cad1-168">Vea también</span><span class="sxs-lookup"><span data-stu-id="2cad1-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cad1-169">**DlgDirList**</span><span class="sxs-lookup"><span data-stu-id="2cad1-169">**DlgDirList**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista)
</dt> </dl>

 

 





