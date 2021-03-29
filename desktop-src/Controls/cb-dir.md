---
title: Mensaje de CB_DIR (Winuser. h)
description: Agrega nombres a la lista mostrada por el cuadro combinado. El mensaje agrega los nombres de los directorios y archivos que coinciden con una cadena y un conjunto de atributos de archivo especificados. \_El directorio CB también puede Agregar Letras de unidad asignadas a la lista.
ms.assetid: 6082d12c-0af4-4a99-98c0-6a98d171f4d8
keywords:
- CB_DIR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- CB_DIR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98cbea5bb88614d5606dd3d5cb165be59f632556
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905246"
---
# <a name="cb_dir-message"></a><span data-ttu-id="cebab-106">Mensaje de Dir. CB \_</span><span class="sxs-lookup"><span data-stu-id="cebab-106">CB\_DIR message</span></span>

<span data-ttu-id="cebab-107">Agrega nombres a la lista mostrada por el cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="cebab-107">Adds names to the list displayed by the combo box.</span></span> <span data-ttu-id="cebab-108">El mensaje agrega los nombres de los directorios y archivos que coinciden con una cadena y un conjunto de atributos de archivo especificados.</span><span class="sxs-lookup"><span data-stu-id="cebab-108">The message adds the names of directories and files that match a specified string and set of file attributes.</span></span> <span data-ttu-id="cebab-109">**CB \_ DIR** también puede Agregar Letras de unidad asignadas a la lista.</span><span class="sxs-lookup"><span data-stu-id="cebab-109">**CB\_DIR** can also add mapped drive letters to the list.</span></span>

## <a name="parameters"></a><span data-ttu-id="cebab-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cebab-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cebab-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cebab-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cebab-112">Atributos de los archivos o directorios que se van a agregar al cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="cebab-112">The attributes of the files or directories to be added to the combo box.</span></span> <span data-ttu-id="cebab-113">Este parámetro puede ser uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="cebab-113">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="cebab-114">Value</span><span class="sxs-lookup"><span data-stu-id="cebab-114">Value</span></span>                                                                                                                                                         | <span data-ttu-id="cebab-115">Significado</span><span class="sxs-lookup"><span data-stu-id="cebab-115">Meaning</span></span>                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DDL_ARCHIVE"></span><span id="ddl_archive"></span><dl> <span data-ttu-id="cebab-116"><dt>**\_archivo DDL**</dt></span><span class="sxs-lookup"><span data-stu-id="cebab-116"><dt>**DDL\_ARCHIVE**</dt></span></span> </dl>       | <span data-ttu-id="cebab-117">Incluye archivos archivados.</span><span class="sxs-lookup"><span data-stu-id="cebab-117">Includes archived files.</span></span><br/>                                                                                                            |
| <span id="DDL_DIRECTORY"></span><span id="ddl_directory"></span><dl> <span data-ttu-id="cebab-118"><dt>**\_directorio DDL**</dt></span><span class="sxs-lookup"><span data-stu-id="cebab-118"><dt>**DDL\_DIRECTORY**</dt></span></span> </dl> | <span data-ttu-id="cebab-119">Incluye subdirectorios, que se incluyen entre corchetes ( \[ \] ).</span><span class="sxs-lookup"><span data-stu-id="cebab-119">Includes subdirectories, which are enclosed in square brackets (\[ \]).</span></span><br/>                                                             |
| <span id="DDL_DRIVES"></span><span id="ddl_drives"></span><dl> <span data-ttu-id="cebab-120"><dt>**\_unidades DDL**</dt></span><span class="sxs-lookup"><span data-stu-id="cebab-120"><dt>**DDL\_DRIVES**</dt></span></span> </dl>          | <span data-ttu-id="cebab-121">Todas las unidades asignadas se agregan a la lista.</span><span class="sxs-lookup"><span data-stu-id="cebab-121">All mapped drives are added to the list.</span></span> <span data-ttu-id="cebab-122">Las unidades se muestran en el formato \[ - *x* - \] , donde *x* es la letra de la unidad.</span><span class="sxs-lookup"><span data-stu-id="cebab-122">Drives are listed in the form \[-*x*-\], where *x* is the drive letter.</span></span><br/>                    |
| <span id="DDL_EXCLUSIVE"></span><span id="ddl_exclusive"></span><dl> <span data-ttu-id="cebab-123"><dt>**DDL \_ exclusivo**</dt></span><span class="sxs-lookup"><span data-stu-id="cebab-123"><dt>**DDL\_EXCLUSIVE**</dt></span></span> </dl> | <span data-ttu-id="cebab-124">Incluye solo los archivos con los atributos especificados.</span><span class="sxs-lookup"><span data-stu-id="cebab-124">Includes only files with the specified attributes.</span></span> <span data-ttu-id="cebab-125">De forma predeterminada, los archivos de lectura y escritura se enumeran incluso si \_ no se especifica DDL ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="cebab-125">By default, read/write files are listed even if DDL\_READWRITE is not specified.</span></span><br/> |
| <span id="DDL_HIDDEN"></span><span id="ddl_hidden"></span><dl> <span data-ttu-id="cebab-126"><dt>**DDL \_ oculto**</dt></span><span class="sxs-lookup"><span data-stu-id="cebab-126"><dt>**DDL\_HIDDEN**</dt></span></span> </dl>          | <span data-ttu-id="cebab-127">Incluye archivos ocultos.</span><span class="sxs-lookup"><span data-stu-id="cebab-127">Includes hidden files.</span></span><br/>                                                                                                              |
| <span id="DDL_READONLY"></span><span id="ddl_readonly"></span><dl> <span data-ttu-id="cebab-128"><dt>**DDL de \_ solo lectura**</dt></span><span class="sxs-lookup"><span data-stu-id="cebab-128"><dt>**DDL\_READONLY**</dt></span></span> </dl>    | <span data-ttu-id="cebab-129">Incluye archivos de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="cebab-129">Includes read-only files.</span></span><br/>                                                                                                           |
| <span id="DDL_READWRITE"></span><span id="ddl_readwrite"></span><dl> <span data-ttu-id="cebab-130"><dt>**ReadWrite de DDL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cebab-130"><dt>**DDL\_READWRITE**</dt></span></span> </dl> | <span data-ttu-id="cebab-131">Incluye archivos de lectura/escritura sin atributos adicionales.</span><span class="sxs-lookup"><span data-stu-id="cebab-131">Includes read/write files with no additional attributes.</span></span> <span data-ttu-id="cebab-132">Este es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="cebab-132">This is the default.</span></span><br/>                                                       |
| <span id="DDL_SYSTEM"></span><span id="ddl_system"></span><dl> <span data-ttu-id="cebab-133"><dt>**\_sistema DDL**</dt></span><span class="sxs-lookup"><span data-stu-id="cebab-133"><dt>**DDL\_SYSTEM**</dt></span></span> </dl>          | <span data-ttu-id="cebab-134">Incluye archivos del sistema.</span><span class="sxs-lookup"><span data-stu-id="cebab-134">Includes system files.</span></span><br/>                                                                                                              |



 

</dd> <dt>

<span data-ttu-id="cebab-135">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cebab-135">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cebab-136">Un puntero **LPCTSTR** a una cadena terminada en null que especifica una ruta de acceso absoluta, una ruta de acceso relativa o un nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="cebab-136">An **LPCTSTR** pointer to a null-terminated string that specifies an absolute path, relative path, or file name.</span></span> <span data-ttu-id="cebab-137">Una ruta de acceso absoluta puede empezar con una letra de unidad (por ejemplo, d: \) o un nombre UNC (por ejemplo, \\ \\ *MachineName* \\ *ShareName*).</span><span class="sxs-lookup"><span data-stu-id="cebab-137">An absolute path can begin with a drive letter (for example, d:\) or a UNC name (for example, \\\\*machinename*\\*sharename*).</span></span> <span data-ttu-id="cebab-138">Si la cadena especifica un nombre de archivo o un directorio que tiene los atributos especificados por el parámetro *wParam* , el nombre de archivo o el directorio se agregan a la lista.</span><span class="sxs-lookup"><span data-stu-id="cebab-138">If the string specifies a file name or directory that has the attributes specified by the *wParam* parameter, the file name or directory is added to the list.</span></span> <span data-ttu-id="cebab-139">Si el nombre de archivo o el nombre de directorio contiene caracteres comodín (?</span><span class="sxs-lookup"><span data-stu-id="cebab-139">If the file name or directory name contains wildcard characters (?</span></span> <span data-ttu-id="cebab-140">o \* ), todos los archivos o directorios que coinciden con la expresión de carácter comodín y que tienen los atributos especificados por el parámetro *wParam* se agregan a la lista mostrada en el cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="cebab-140">or \*), all files or directories that match the wildcard expression and have the attributes specified by the *wParam* parameter are added to the list displayed in the combo box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cebab-141">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cebab-141">Return value</span></span>

<span data-ttu-id="cebab-142">Si el mensaje se realiza correctamente, el valor devuelto es el índice de base cero del último nombre agregado a la lista.</span><span class="sxs-lookup"><span data-stu-id="cebab-142">If the message succeeds, the return value is the zero-based index of the last name added to the list.</span></span>

<span data-ttu-id="cebab-143">Si se produce un error, el valor devuelto es CB \_ error.</span><span class="sxs-lookup"><span data-stu-id="cebab-143">If an error occurs, the return value is CB\_ERR.</span></span> <span data-ttu-id="cebab-144">Si no hay suficiente espacio para almacenar las nuevas cadenas, el valor devuelto es CB \_ ERRSPACE.</span><span class="sxs-lookup"><span data-stu-id="cebab-144">If there is insufficient space to store the new strings, the return value is CB\_ERRSPACE.</span></span>

## <a name="remarks"></a><span data-ttu-id="cebab-145">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cebab-145">Remarks</span></span>

<span data-ttu-id="cebab-146">Si *wParam* incluye la \_ marca de directorio DDL y *lParam* especifica todos los subdirectorios de un directorio de primer nivel, como C: \\ temp \\ \* , el cuadro de lista incluirá siempre una entrada ".." para el directorio raíz.</span><span class="sxs-lookup"><span data-stu-id="cebab-146">If *wParam* includes the DDL\_DIRECTORY flag and *lParam* specifies all the subdirectories of a first-level directory, such as C:\\TEMP\\\*, the list box will always include a ".." entry for the root directory.</span></span> <span data-ttu-id="cebab-147">Esto es así incluso si el directorio raíz tiene atributos ocultos o del sistema, y \_ \_ no se especifican las marcas DDL ocultas y del sistema DDL.</span><span class="sxs-lookup"><span data-stu-id="cebab-147">This is true even if the root directory has hidden or system attributes and the DDL\_HIDDEN and DDL\_SYSTEM flags are not specified.</span></span> <span data-ttu-id="cebab-148">El directorio raíz de un volumen NTFS tiene atributos ocultos y del sistema.</span><span class="sxs-lookup"><span data-stu-id="cebab-148">The root directory of an NTFS volume has hidden and system attributes.</span></span>

<span data-ttu-id="cebab-149">La lista muestra los nombres de archivo largos, si los hay.</span><span class="sxs-lookup"><span data-stu-id="cebab-149">The list displays long file names, if any.</span></span>

## <a name="requirements"></a><span data-ttu-id="cebab-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cebab-150">Requirements</span></span>



| <span data-ttu-id="cebab-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="cebab-151">Requirement</span></span> | <span data-ttu-id="cebab-152">Value</span><span class="sxs-lookup"><span data-stu-id="cebab-152">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cebab-153">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cebab-153">Minimum supported client</span></span><br/> | <span data-ttu-id="cebab-154">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="cebab-154">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cebab-155">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cebab-155">Minimum supported server</span></span><br/> | <span data-ttu-id="cebab-156">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="cebab-156">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cebab-157">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cebab-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="cebab-158"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cebab-158"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cebab-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="cebab-159">See also</span></span>

<dl> <dt>

<span data-ttu-id="cebab-160">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="cebab-160">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cebab-161">**CB \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="cebab-161">**CB\_ADDSTRING**</span></span>](cb-addstring.md)
</dt> <dt>

[<span data-ttu-id="cebab-162">**CB \_ INSERTSTRING**</span><span class="sxs-lookup"><span data-stu-id="cebab-162">**CB\_INSERTSTRING**</span></span>](cb-insertstring.md)
</dt> <dt>

[<span data-ttu-id="cebab-163">**DlgDirListComboBox**</span><span class="sxs-lookup"><span data-stu-id="cebab-163">**DlgDirListComboBox**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dlgdirlistcomboboxa)
</dt> </dl>

 

 





