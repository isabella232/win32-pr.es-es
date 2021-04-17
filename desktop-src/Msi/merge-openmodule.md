---
description: El método OpenModule del objeto Merge abre un módulo de combinación de Windows Installer en modo de solo lectura. Un módulo debe estar abierto antes de que se pueda combinar con una base de datos de instalación.
ms.assetid: fc976899-2c39-4314-b2fb-417e0dfc53b9
title: Merge. OpenModule (método) (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.OpenModule
- IMsmMerge.OpenModule
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 9d83a9331c91817f70c49ecf74c7171c5e627be6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681305"
---
# <a name="mergeopenmodule-method"></a><span data-ttu-id="4c7b7-104">Merge. OpenModule (método)</span><span class="sxs-lookup"><span data-stu-id="4c7b7-104">Merge.OpenModule method</span></span>

<span data-ttu-id="4c7b7-105">El método **OpenModule** del objeto [**Merge**](merge-object.md) abre un módulo de combinación de Windows Installer en modo de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4c7b7-105">The **OpenModule** method of the [**Merge**](merge-object.md) object opens a Windows Installer merge module in read-only mode.</span></span> <span data-ttu-id="4c7b7-106">Un módulo debe estar abierto antes de que se pueda combinar con una base de datos de instalación.</span><span class="sxs-lookup"><span data-stu-id="4c7b7-106">A module must be opened before it can be merged with an installation database.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c7b7-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4c7b7-107">Syntax</span></span>


```JScript
Merge.OpenModule(
  FileName,
  Language
)
```



## <a name="parameters"></a><span data-ttu-id="4c7b7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4c7b7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c7b7-109">*FileName*</span><span class="sxs-lookup"><span data-stu-id="4c7b7-109">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="4c7b7-110">Nombre de archivo completo que apunta a un módulo de combinación.</span><span class="sxs-lookup"><span data-stu-id="4c7b7-110">Fully qualified file name pointing to a merge module.</span></span>

</dd> <dt>

<span data-ttu-id="4c7b7-111">*Lenguaje*</span><span class="sxs-lookup"><span data-stu-id="4c7b7-111">*Language*</span></span> 
</dt> <dd>

<span data-ttu-id="4c7b7-112">Identificador de idioma (LANGID) válido.</span><span class="sxs-lookup"><span data-stu-id="4c7b7-112">A valid language identifier (LANGID).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c7b7-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4c7b7-113">Return value</span></span>

<span data-ttu-id="4c7b7-114">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="4c7b7-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c7b7-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4c7b7-115">Remarks</span></span>

<span data-ttu-id="4c7b7-116">Esta función abre el módulo de combinación en modo de solo lectura y evita que otros programas escriban en el módulo de combinación hasta que se llama al método [**CloseModule**](merge-closemodule.md) .</span><span class="sxs-lookup"><span data-stu-id="4c7b7-116">This function opens the merge module in read-only mode and excludes other programs from writing to the merge module until the [**CloseModule**](merge-closemodule.md) method is called.</span></span>

<span data-ttu-id="4c7b7-117">El instalador intenta abrir el módulo en el idioma especificado por *Language* o en un lenguaje más general.</span><span class="sxs-lookup"><span data-stu-id="4c7b7-117">The installer attempts to open the module in the language specified by *Language*, or a more general language.</span></span> <span data-ttu-id="4c7b7-118">Por ejemplo, si *Language* se especifica como 1033, se puede abrir un módulo con un idioma predeterminado de 1033, 9 o 0 en su idioma predeterminado.</span><span class="sxs-lookup"><span data-stu-id="4c7b7-118">For example, if *Language* is specified as 1033, a module with a default language of 1033, 9, or 0 can be opened in its default language.</span></span> <span data-ttu-id="4c7b7-119">Un valor de *idioma* de 9 abre los módulos con un idioma predeterminado de 9 o 0.</span><span class="sxs-lookup"><span data-stu-id="4c7b7-119">A *Language* value of 9 opens modules with a default language of 9 or 0.</span></span> <span data-ttu-id="4c7b7-120">Si el idioma predeterminado del módulo no cumple los requisitos especificados, se realiza un intento de transformar el módulo en el idioma solicitado.</span><span class="sxs-lookup"><span data-stu-id="4c7b7-120">If the default language of the module does not meet the specified requirements, an attempt is made to transform the module to the requested language.</span></span> <span data-ttu-id="4c7b7-121">Si se produce un error, el módulo se transforma en lenguajes cada vez más generales, hasta el lenguaje neutro.</span><span class="sxs-lookup"><span data-stu-id="4c7b7-121">If that fails, the module is transformed to increasingly general languages, all the way to language neutral.</span></span> <span data-ttu-id="4c7b7-122">Si ninguna de las transformaciones se realiza correctamente, el módulo no se abre.</span><span class="sxs-lookup"><span data-stu-id="4c7b7-122">If none of the transforms succeed, the module fails to open.</span></span> <span data-ttu-id="4c7b7-123">En este caso, se agrega un error a la lista de errores de tipo msmErrorLanguageUnsupported.</span><span class="sxs-lookup"><span data-stu-id="4c7b7-123">In this case, an error is added to the error list of type msmErrorLanguageUnsupported.</span></span> <span data-ttu-id="4c7b7-124">Si se produce un error al transformar el módulo en el idioma deseado, se agrega un error a la lista de errores de tipo msmErrorLanguageFailed.</span><span class="sxs-lookup"><span data-stu-id="4c7b7-124">If there is an error transforming the module to the desired language, an error is added to the error list of type msmErrorLanguageFailed.</span></span> <span data-ttu-id="4c7b7-125">Para obtener más información, vea la propiedad [**Type**](error-type.md) del objeto [**error**](error-object.md) .</span><span class="sxs-lookup"><span data-stu-id="4c7b7-125">For details, see the [**Type**](error-type.md) property of the [**Error**](error-object.md) object.</span></span> <span data-ttu-id="4c7b7-126">Al abrir un módulo de combinación, se borran los errores que aún no se han recuperado.</span><span class="sxs-lookup"><span data-stu-id="4c7b7-126">Opening a merge module clears any errors that have not already been retrieved.</span></span>

### <a name="c"></a><span data-ttu-id="4c7b7-127">C++</span><span class="sxs-lookup"><span data-stu-id="4c7b7-127">C++</span></span>

<span data-ttu-id="4c7b7-128">Consulte función [**OpenModule**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openmodule) .</span><span class="sxs-lookup"><span data-stu-id="4c7b7-128">See [**OpenModule**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openmodule) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c7b7-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c7b7-129">Requirements</span></span>



| <span data-ttu-id="4c7b7-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c7b7-130">Requirement</span></span> | <span data-ttu-id="4c7b7-131">Value</span><span class="sxs-lookup"><span data-stu-id="4c7b7-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c7b7-132">Versión</span><span class="sxs-lookup"><span data-stu-id="4c7b7-132">Version</span></span><br/> | <span data-ttu-id="4c7b7-133">Mergemod.dll 1,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="4c7b7-133">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="4c7b7-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4c7b7-134">Header</span></span><br/>  | <dl> <span data-ttu-id="4c7b7-135"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c7b7-135"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="4c7b7-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4c7b7-136">DLL</span></span><br/>     | <dl> <span data-ttu-id="4c7b7-137"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c7b7-137"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
