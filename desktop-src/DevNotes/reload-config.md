---
description: Vuelve a cargar una configuración de IME desde el registro HKCU, solo en el IME japonés.
ms.assetid: 171c31ad-c925-4e18-b458-d9abf52dae9a
title: reload_config función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- reload_config
api_type:
- DllExport
api_location:
- Imejpknl.dll
- Imejp98k.dll
ms.openlocfilehash: bc9d0d026359036d8847ebaa2542f778de4d5767
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671615"
---
# <a name="reload_config-function"></a><span data-ttu-id="67f45-103">recargar la \_ función de configuración</span><span class="sxs-lookup"><span data-stu-id="67f45-103">reload\_config function</span></span>

<span data-ttu-id="67f45-104">Vuelve a cargar una configuración de IME desde el registro HKCU, solo en el IME japonés.</span><span class="sxs-lookup"><span data-stu-id="67f45-104">Reloads an IME configuration from the HKCU registry, in Japanese IME only.</span></span>

## <a name="syntax"></a><span data-ttu-id="67f45-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="67f45-105">Syntax</span></span>


```C++
BOOL reload_config(void);
```



## <a name="parameters"></a><span data-ttu-id="67f45-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="67f45-106">Parameters</span></span>

<span data-ttu-id="67f45-107">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="67f45-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="67f45-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="67f45-108">Return value</span></span>

<span data-ttu-id="67f45-109">Esta función devuelve **true** si se realiza correctamente; de lo contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="67f45-109">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="67f45-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="67f45-110">Remarks</span></span>

<span data-ttu-id="67f45-111">Si no hay ningún valor del registro en HKCU, la función de **\_ configuración Reload** escribe los datos iniciales en el registro.</span><span class="sxs-lookup"><span data-stu-id="67f45-111">If no registry value is present in HKCU, the **reload\_config** function writes initial data to the registry.</span></span>

<span data-ttu-id="67f45-112">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="67f45-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="67f45-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67f45-113">Requirements</span></span>



| <span data-ttu-id="67f45-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="67f45-114">Requirement</span></span> | <span data-ttu-id="67f45-115">Value</span><span class="sxs-lookup"><span data-stu-id="67f45-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67f45-116">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="67f45-116">DLL</span></span><br/> | <dl> <span data-ttu-id="67f45-117"><dt>Imejpknl.dll; </dt> <dt>Imejp98k.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67f45-117"><dt>Imejpknl.dll; </dt> <dt>Imejp98k.dll</dt></span></span> </dl> |



 

 
