---
description: Recupera el título de archivo de la ruta de acceso de archivo especificada.
ms.assetid: 9a559d71-4883-4905-b3ad-64b256a2f51e
title: pSetupGetFileTitle función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupGetFileTitle
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 0b7869833a66799a4e617557cdfe6fdab9d64f67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649543"
---
# <a name="psetupgetfiletitle-function"></a><span data-ttu-id="8282b-103">pSetupGetFileTitle función)</span><span class="sxs-lookup"><span data-stu-id="8282b-103">pSetupGetFileTitle function</span></span>

<span data-ttu-id="8282b-104">\[Esta función no está disponible en Windows Vista ni Windows Server 2008.\]</span><span class="sxs-lookup"><span data-stu-id="8282b-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="8282b-105">Recupera el título de archivo de la ruta de acceso de archivo especificada.</span><span class="sxs-lookup"><span data-stu-id="8282b-105">Retrieves the file title for the specified file path.</span></span>

## <a name="syntax"></a><span data-ttu-id="8282b-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8282b-106">Syntax</span></span>


```C++
PCTSTR pSetupGetFileTitle(
  _In_ PCTSTR FilePath
);
```



## <a name="parameters"></a><span data-ttu-id="8282b-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8282b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8282b-108">*FilePath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8282b-108">*FilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8282b-109">Ruta de acceso al archivo.</span><span class="sxs-lookup"><span data-stu-id="8282b-109">The file path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8282b-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8282b-110">Return value</span></span>

<span data-ttu-id="8282b-111">Un puntero a una cadena que recibe el título del archivo.</span><span class="sxs-lookup"><span data-stu-id="8282b-111">A pointer to string that receives the file title.</span></span>

## <a name="remarks"></a><span data-ttu-id="8282b-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8282b-112">Remarks</span></span>

<span data-ttu-id="8282b-113">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="8282b-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="8282b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8282b-114">Requirements</span></span>



| <span data-ttu-id="8282b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8282b-115">Requirement</span></span> | <span data-ttu-id="8282b-116">Value</span><span class="sxs-lookup"><span data-stu-id="8282b-116">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8282b-117">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8282b-117">DLL</span></span><br/> | <dl> <span data-ttu-id="8282b-118"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8282b-118"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
