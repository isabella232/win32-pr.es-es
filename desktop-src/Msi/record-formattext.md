---
description: El método FormatText del objeto record da formato a los campos según la plantilla del campo 0.
ms.assetid: 89a98b88-bb74-458c-a2df-727a8084145b
title: Método record. FormatText
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record.FormatText
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 377a1614d06ab4dfe1fa4f8b0745d420dc4d01ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653834"
---
# <a name="recordformattext-method"></a><span data-ttu-id="cdea7-103">Método record. FormatText</span><span class="sxs-lookup"><span data-stu-id="cdea7-103">Record.FormatText method</span></span>

<span data-ttu-id="cdea7-104">El método **FormatText** del objeto [**Record**](record-object.md) da formato a los campos según la plantilla del campo 0.</span><span class="sxs-lookup"><span data-stu-id="cdea7-104">The **FormatText** method of the [**Record**](record-object.md) object formats fields according to the template in field 0.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdea7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cdea7-105">Syntax</span></span>


```JScript
Record.FormatText()
```



## <a name="parameters"></a><span data-ttu-id="cdea7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cdea7-106">Parameters</span></span>

<span data-ttu-id="cdea7-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="cdea7-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cdea7-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cdea7-108">Return value</span></span>

<span data-ttu-id="cdea7-109">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="cdea7-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cdea7-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cdea7-110">Remarks</span></span>

<span data-ttu-id="cdea7-111">El método **FormatText** sigue la funcionalidad de la función [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) si se pasa a **MsiFormatRecord** un identificador de instalador NULL como su primer parámetro.</span><span class="sxs-lookup"><span data-stu-id="cdea7-111">The **FormatText** method follows the functionality of the [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) function if **MsiFormatRecord** was passed a null installer handle as its first parameter.</span></span> <span data-ttu-id="cdea7-112">Como resultado, solo se procesan los parámetros de campo de registro y las propiedades no están disponibles para la sustitución.</span><span class="sxs-lookup"><span data-stu-id="cdea7-112">As a result, only the record field parameters are processed and properties are not available for substitution.</span></span>

<span data-ttu-id="cdea7-113">Por ejemplo, una cadena como "dar formato a este campo: \[ 1 \] , dar formato a esta propiedad \[ \] " se resuelve como "dar formato a este campo: valor de campo 1, dar formato a esta propiedad: \[ propiedad \] ".</span><span class="sxs-lookup"><span data-stu-id="cdea7-113">For example, a string such as "format this field: \[1\], format this property: \[property\]" is resolved to "format this field: value from field 1, format this property: \[property\]."</span></span>

<span data-ttu-id="cdea7-114">Los parámetros a los que se va a [dar formato](formatted.md) se incluyen entre corchetes \[ ... \] .</span><span class="sxs-lookup"><span data-stu-id="cdea7-114">Parameters that are to be [formatted](formatted.md) are enclosed in square brackets \[...\].</span></span> <span data-ttu-id="cdea7-115">Los corchetes se pueden iterar porque las sustituciones se resuelven desde el interior.</span><span class="sxs-lookup"><span data-stu-id="cdea7-115">The square brackets can be iterated because the substitutions are resolved from the inside out.</span></span>

<span data-ttu-id="cdea7-116">Si una parte de la cadena está entre llaves {} y no contiene corchetes, se deja sin cambios, incluidas las llaves.</span><span class="sxs-lookup"><span data-stu-id="cdea7-116">If a part of the string is enclosed in curly braces { } and contains no square brackets, it is left unchanged, including the curly braces.</span></span>

<span data-ttu-id="cdea7-117">Nota en el caso de [las acciones personalizadas de ejecución aplazada](deferred-execution-custom-actions.md), **FormatText** solo admite un conjunto limitado de propiedades: las propiedades CustomActionData y ProductCode.</span><span class="sxs-lookup"><span data-stu-id="cdea7-117">Note in the case of [deferred execution custom actions](deferred-execution-custom-actions.md), **FormatText** only supports a limited set of properties: the CustomActionData and ProductCode properties.</span></span> <span data-ttu-id="cdea7-118">Para obtener más información, vea [obtener información de contexto para las acciones personalizadas de ejecución aplazada](obtaining-context-information-for-deferred-execution-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="cdea7-118">For more information, see [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cdea7-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cdea7-119">Requirements</span></span>



| <span data-ttu-id="cdea7-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="cdea7-120">Requirement</span></span> | <span data-ttu-id="cdea7-121">Value</span><span class="sxs-lookup"><span data-stu-id="cdea7-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdea7-122">Versión</span><span class="sxs-lookup"><span data-stu-id="cdea7-122">Version</span></span><br/> | <span data-ttu-id="cdea7-123">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cdea7-123">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="cdea7-124">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cdea7-124">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="cdea7-125">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="cdea7-125">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="cdea7-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cdea7-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="cdea7-127"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cdea7-127"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="cdea7-128">IID</span><span class="sxs-lookup"><span data-stu-id="cdea7-128">IID</span></span><br/>     | <span data-ttu-id="cdea7-129">IID \_ IRecord se define como 000C1093-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="cdea7-129">IID\_IRecord is defined as 000C1093-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                              |



## <a name="see-also"></a><span data-ttu-id="cdea7-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="cdea7-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdea7-131">**MsiFormatRecord**</span><span class="sxs-lookup"><span data-stu-id="cdea7-131">**MsiFormatRecord**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda)
</dt> <dt>

[<span data-ttu-id="cdea7-132">Formatea</span><span class="sxs-lookup"><span data-stu-id="cdea7-132">Formatted</span></span>](formatted.md)
</dt> <dt>

[<span data-ttu-id="cdea7-133">Tipos de datos de columna</span><span class="sxs-lookup"><span data-stu-id="cdea7-133">Column Data Types</span></span>](column-data-types.md)
</dt> </dl>

 

 




