---
description: El método GetError del objeto View devuelve el error de validación y el nombre de columna para los que se produjo el error.
ms.assetid: ca90dfa5-8e15-490c-835b-c5c225c3cc7b
title: View. GetError (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- View.GetError
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1305bf6f497e92ff4d455a696179a943df8a057b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653481"
---
# <a name="viewgeterror-method"></a><span data-ttu-id="3bf7c-103">View. GetError (método)</span><span class="sxs-lookup"><span data-stu-id="3bf7c-103">View.GetError method</span></span>

<span data-ttu-id="3bf7c-104">El método **GetError** del objeto [**View**](view-object.md) devuelve el error de validación y el nombre de columna para los que se produjo el error.</span><span class="sxs-lookup"><span data-stu-id="3bf7c-104">The **GetError** method of the [**View**](view-object.md) object returns the Validation error and the column name for which the error occurred.</span></span> <span data-ttu-id="3bf7c-105">En Automation, el valor devuelto es una cadena con el formato \# \# columnName, donde \# \# representa un código de error de 2 dígitos.</span><span class="sxs-lookup"><span data-stu-id="3bf7c-105">In automation, the returned value is a string of the form \#\#ColumnName, where the \#\# represents a 2-digit error code.</span></span> <span data-ttu-id="3bf7c-106">Devuelve el primer error en la matriz de errores de la vista. las llamadas subsiguientes devuelven el siguiente valor en la matriz de errores.</span><span class="sxs-lookup"><span data-stu-id="3bf7c-106">It returns the first error in the view's error array; subsequent calls return the next value in the error array.</span></span> <span data-ttu-id="3bf7c-107">Una vez que se devuelve el valor ' 00 ', no existen más errores y las llamadas subsiguientes simplemente recorren en bucle la matriz.</span><span class="sxs-lookup"><span data-stu-id="3bf7c-107">Once a value of '00' is returned, no more errors exist, and subsequent calls merely loop through the array again.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bf7c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3bf7c-108">Syntax</span></span>


```JScript
View.GetError()
```



## <a name="parameters"></a><span data-ttu-id="3bf7c-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3bf7c-109">Parameters</span></span>

<span data-ttu-id="3bf7c-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="3bf7c-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3bf7c-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3bf7c-111">Return value</span></span>

<span data-ttu-id="3bf7c-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="3bf7c-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3bf7c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3bf7c-113">Requirements</span></span>



| <span data-ttu-id="3bf7c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3bf7c-114">Requirement</span></span> | <span data-ttu-id="3bf7c-115">Value</span><span class="sxs-lookup"><span data-stu-id="3bf7c-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3bf7c-116">Versión</span><span class="sxs-lookup"><span data-stu-id="3bf7c-116">Version</span></span><br/> | <span data-ttu-id="3bf7c-117">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3bf7c-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="3bf7c-118">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3bf7c-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="3bf7c-119">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="3bf7c-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="3bf7c-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3bf7c-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="3bf7c-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3bf7c-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="3bf7c-122">IID</span><span class="sxs-lookup"><span data-stu-id="3bf7c-122">IID</span></span><br/>     | <span data-ttu-id="3bf7c-123">IID \_ iView se define como 000C109C-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="3bf7c-123">IID\_IView is defined as 000C109C-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



 

 




