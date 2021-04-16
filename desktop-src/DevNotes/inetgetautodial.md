---
description: La función InetGetAutodial devuelve la configuración de marcado automático del registro.
ms.assetid: e36761da-c050-4844-ad94-efdc77702f6f
title: InetGetAutodial función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InetGetAutodial
api_type:
- DllExport
api_location:
- Inetcfg.dll
ms.openlocfilehash: 15267cd00940f0386c8a5d9c0c54b070f2cff509
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671399"
---
# <a name="inetgetautodial-function"></a><span data-ttu-id="0e661-103">InetGetAutodial función)</span><span class="sxs-lookup"><span data-stu-id="0e661-103">InetGetAutodial function</span></span>

<span data-ttu-id="0e661-104">\[Esta función no se admite y puede modificarse o no estar disponible en versiones futuras de Windows.</span><span class="sxs-lookup"><span data-stu-id="0e661-104">\[This function is unsupported and may be altered or unavailable in future versions of Windows.</span></span> <span data-ttu-id="0e661-105">\]</span><span class="sxs-lookup"><span data-stu-id="0e661-105">\]</span></span>

<span data-ttu-id="0e661-106">La función **InetGetAutodial** devuelve la configuración de marcado automático del registro.</span><span class="sxs-lookup"><span data-stu-id="0e661-106">The **InetGetAutodial** function returns the autodial settings from the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e661-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0e661-107">Syntax</span></span>


```C++
HRESULT InetGetAutodial(
  _Out_ LPBOOL lpfEnable,
  _Out_ LPSTR  lpszEntryName,
  _In_  DWORD  cbEntryNameSize
);
```



## <a name="parameters"></a><span data-ttu-id="0e661-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0e661-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e661-109">*lpfEnable* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0e661-109">*lpfEnable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0e661-110">Indica si el marcado automático está habilitado.</span><span class="sxs-lookup"><span data-stu-id="0e661-110">Indicates whether autodial is enabled.</span></span> <span data-ttu-id="0e661-111">Un valor de **true** cuando se devuelve indica que el marcado automático está habilitado.</span><span class="sxs-lookup"><span data-stu-id="0e661-111">A value of **TRUE** upon return indicates autodial is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="0e661-112">*lpszEntryName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0e661-112">*lpszEntryName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0e661-113">En la devolución, contiene el nombre de la entrada de la libreta de teléfonos que se establece para el marcado automático.</span><span class="sxs-lookup"><span data-stu-id="0e661-113">On return, contains the name of the phone book entry that is set for autodial.</span></span>

</dd> <dt>

<span data-ttu-id="0e661-114">*cbEntryNameSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0e661-114">*cbEntryNameSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e661-115">Tamaño del búfer asignado por el llamador para el nombre de la entrada de la libreta de teléfonos.</span><span class="sxs-lookup"><span data-stu-id="0e661-115">Size of the buffer allocated by the caller for the phone book entry name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e661-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0e661-116">Return value</span></span>

<span data-ttu-id="0e661-117">Esta función puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="0e661-117">This function can return one of these values.</span></span>



| <span data-ttu-id="0e661-118">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="0e661-118">Return code</span></span>                                                                                                | <span data-ttu-id="0e661-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="0e661-119">Description</span></span>                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0e661-120"><dt>**ERROR \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="0e661-120"><dt>**ERROR\_SUCCESS**</dt></span></span> </dl>              | <span data-ttu-id="0e661-121">La llamada se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="0e661-121">The call was successful.</span></span><br/>                                                                                                                       |
| <dl> <span data-ttu-id="0e661-122"><dt>**ERROR de \_ argumentos no válidos \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0e661-122"><dt>**ERROR\_BAD\_ARGUMENTS**</dt></span></span> </dl>       | <span data-ttu-id="0e661-123">*lpfEnable* o *lpszEntryName* contiene un puntero **nulo** o el valor de *cbEntryNameSize* es cero.</span><span class="sxs-lookup"><span data-stu-id="0e661-123">*lpfEnable* or *lpszEntryName* contains a **NULL** pointer, or the value of *cbEntryNameSize* is zero.</span></span><br/>                                         |
| <dl> <span data-ttu-id="0e661-124"><dt>**ERROR \_ de \_ memoria insuficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0e661-124"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl>  | <span data-ttu-id="0e661-125">Memoria insuficiente para asignar búferes internos.</span><span class="sxs-lookup"><span data-stu-id="0e661-125">There was insufficient memory to allocate internal buffers.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="0e661-126"><dt>**ERROR \_ de \_ búfer insuficiente**</dt></span><span class="sxs-lookup"><span data-stu-id="0e661-126"><dt>**ERROR\_INSUFFICIENT\_BUFFER**</dt></span></span> </dl> | <span data-ttu-id="0e661-127">*cbEntryNameSize* no indica que el búfer señalado por *lpszEntryName* es lo suficientemente grande como para recibir el nombre de la entrada de la libreta de teléfonos.</span><span class="sxs-lookup"><span data-stu-id="0e661-127">*cbEntryNameSize* does not indicate that the buffer pointed to by *lpszEntryName* is large enough to receive the name of the phone book entry.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0e661-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0e661-128">Remarks</span></span>

<span data-ttu-id="0e661-129">Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="0e661-129">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e661-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e661-130">Requirements</span></span>



| <span data-ttu-id="0e661-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e661-131">Requirement</span></span> | <span data-ttu-id="0e661-132">Value</span><span class="sxs-lookup"><span data-stu-id="0e661-132">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0e661-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0e661-133">DLL</span></span><br/> | <dl> <span data-ttu-id="0e661-134"><dt>Inetcfg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e661-134"><dt>Inetcfg.dll</dt></span></span> </dl> |



 

 
