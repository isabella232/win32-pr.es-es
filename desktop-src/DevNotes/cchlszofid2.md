---
description: Descodifica y almacena una cadena.
ms.assetid: 6ababd6e-57b7-49eb-98c9-a4bcb558a377
title: CchLszOfId2 función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CchLszOfId2
api_type:
- DllExport
api_location:
- Msjint40.dll
ms.openlocfilehash: cba2d09f9865c43a5b64a34783c621c783c7aac3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661063"
---
# <a name="cchlszofid2-function"></a><span data-ttu-id="70c30-103">CchLszOfId2 función)</span><span class="sxs-lookup"><span data-stu-id="70c30-103">CchLszOfId2 function</span></span>

<span data-ttu-id="70c30-104">Descodifica y almacena una cadena.</span><span class="sxs-lookup"><span data-stu-id="70c30-104">Decodes and stores a string.</span></span>

## <a name="syntax"></a><span data-ttu-id="70c30-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="70c30-105">Syntax</span></span>


```C++
UINT CchLszOfId2(
   UINT  id,
   WCHAR *lsz,
   UINT  cbmax
);
```



## <a name="parameters"></a><span data-ttu-id="70c30-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="70c30-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70c30-107">*id*</span><span class="sxs-lookup"><span data-stu-id="70c30-107">*id*</span></span> 
</dt> <dd>

<span data-ttu-id="70c30-108">El identificador de la cadena en el archivo de recursos que se va a descodificar y almacenar.</span><span class="sxs-lookup"><span data-stu-id="70c30-108">The identifier of the string in the resource file to be decoded and stored.</span></span> <span data-ttu-id="70c30-109">No se comprueba la validez de la cadena.</span><span class="sxs-lookup"><span data-stu-id="70c30-109">The validity of the string is not verified.</span></span>

</dd> <dt>

<span data-ttu-id="70c30-110">*lsz*</span><span class="sxs-lookup"><span data-stu-id="70c30-110">*lsz*</span></span> 
</dt> <dd>

<span data-ttu-id="70c30-111">Un puntero a un búfer con una longitud de *cbmax*.</span><span class="sxs-lookup"><span data-stu-id="70c30-111">A pointer to a buffer with a length of *cbmax*.</span></span> <span data-ttu-id="70c30-112">Las cadenas que son más largas que *cbmax* se truncan.</span><span class="sxs-lookup"><span data-stu-id="70c30-112">Strings that are longer than *cbmax* are truncated.</span></span>

</dd> <dt>

<span data-ttu-id="70c30-113">*cbmax*</span><span class="sxs-lookup"><span data-stu-id="70c30-113">*cbmax*</span></span> 
</dt> <dd>

<span data-ttu-id="70c30-114">Longitud máxima de la cadena que se va a almacenar en el parámetro *LSZ* .</span><span class="sxs-lookup"><span data-stu-id="70c30-114">The maximum length of the string to be stored in the *lsz* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70c30-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="70c30-115">Return value</span></span>

<span data-ttu-id="70c30-116">Esta función devuelve la cadena descodificada.</span><span class="sxs-lookup"><span data-stu-id="70c30-116">This function returns the decoded string.</span></span>

## <a name="remarks"></a><span data-ttu-id="70c30-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="70c30-117">Remarks</span></span>

<span data-ttu-id="70c30-118">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="70c30-118">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="70c30-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70c30-119">Requirements</span></span>



| <span data-ttu-id="70c30-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="70c30-120">Requirement</span></span> | <span data-ttu-id="70c30-121">Value</span><span class="sxs-lookup"><span data-stu-id="70c30-121">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="70c30-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="70c30-122">DLL</span></span><br/> | <dl> <span data-ttu-id="70c30-123"><dt>Msjint40.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70c30-123"><dt>Msjint40.dll</dt></span></span> </dl> |



 

 
