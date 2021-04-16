---
description: Abre un identificador de un objeto de subproceso con el acceso especificado.
ms.assetid: 85148f27-cfb4-4a33-8bcc-e48d2c2e3c51
title: NtOpenThread función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtOpenThread
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 8c1b64d2e024f3905d171ab5ca90e59df929ffc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649837"
---
# <a name="ntopenthread-function"></a><span data-ttu-id="dccc7-103">NtOpenThread función)</span><span class="sxs-lookup"><span data-stu-id="dccc7-103">NtOpenThread function</span></span>

<span data-ttu-id="dccc7-104">\[Esta función se puede cambiar o quitar de Windows sin previo aviso.</span><span class="sxs-lookup"><span data-stu-id="dccc7-104">\[This function may be changed or removed from Windows without further notice.</span></span> <span data-ttu-id="dccc7-105">En su lugar, use la función [**OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) .\]</span><span class="sxs-lookup"><span data-stu-id="dccc7-105">Use the [**OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) function instead.\]</span></span>

<span data-ttu-id="dccc7-106">Abre un identificador de un objeto de subproceso con el acceso especificado.</span><span class="sxs-lookup"><span data-stu-id="dccc7-106">Opens a handle to a thread object with the access specified.</span></span>

## <a name="syntax"></a><span data-ttu-id="dccc7-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dccc7-107">Syntax</span></span>


```C++
NTSTATUS NtOpenThread(
  _Out_ PHANDLE            ThreadHandle,
  _In_  ACCESS_MASK        DesiredAccess,
  _In_  POBJECT_ATTRIBUTES ObjectAttributes,
  _In_  PCLIENT_ID         ClientId
);
```



## <a name="parameters"></a><span data-ttu-id="dccc7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dccc7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dccc7-109">*ThreadHandle* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="dccc7-109">*ThreadHandle* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dccc7-110">Puntero a una variable que recibe el identificador del objeto de subproceso.</span><span class="sxs-lookup"><span data-stu-id="dccc7-110">A pointer to a variable that receives the thread object handle.</span></span>

</dd> <dt>

<span data-ttu-id="dccc7-111">*DesiredAccess* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dccc7-111">*DesiredAccess* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dccc7-112">Un tipo de datos de [**\_ máscara de acceso**](../secauthz/access-mask-format.md) que proporciona los tipos de acceso deseados para el objeto de subproceso.</span><span class="sxs-lookup"><span data-stu-id="dccc7-112">An [**ACCESS\_MASK**](../secauthz/access-mask-format.md) data type that provides the desired types of access for the thread object.</span></span>

</dd> <dt>

<span data-ttu-id="dccc7-113">*ObjectAttributes* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dccc7-113">*ObjectAttributes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dccc7-114">Puntero a una estructura [de \_ atributos de objeto](https://msdn.microsoft.com/library/aa491657.aspx) .</span><span class="sxs-lookup"><span data-stu-id="dccc7-114">A pointer to an [OBJECT\_ATTRIBUTES](https://msdn.microsoft.com/library/aa491657.aspx) structure.</span></span> <span data-ttu-id="dccc7-115">El miembro **objectname** de esta estructura debe ser null.</span><span class="sxs-lookup"><span data-stu-id="dccc7-115">The **ObjectName** member of this structure must be NULL.</span></span>

<span data-ttu-id="dccc7-116">**Windows Server 2003 y Windows XP:** El miembro **objectname** de esta estructura puede apuntar a un nombre de objeto.</span><span class="sxs-lookup"><span data-stu-id="dccc7-116">**Windows Server 2003 and Windows XP:** The **ObjectName** member of this structure can point to an object name.</span></span> <span data-ttu-id="dccc7-117">Si **objectname** no es null, el parámetro *CLIENTID* debe ser null.</span><span class="sxs-lookup"><span data-stu-id="dccc7-117">If **ObjectName** is not NULL, the *ClientId* parameter must be NULL.</span></span>

</dd> <dt>

<span data-ttu-id="dccc7-118">*ClientID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="dccc7-118">*ClientId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dccc7-119">Puntero a una estructura **de \_ identificador de cliente** que identifica el subproceso cuyo subproceso se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="dccc7-119">A pointer to a **CLIENT\_ID** structure that identifies the thread whose thread is to be opened.</span></span>

<span data-ttu-id="dccc7-120">**Windows Server 2003 y Windows XP:** Puntero a una estructura **de \_ identificador de cliente** que identifica el subproceso cuyo subproceso se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="dccc7-120">**Windows Server 2003 and Windows XP:** A pointer to a **CLIENT\_ID** structure that identifies the thread whose thread is to be opened.</span></span> <span data-ttu-id="dccc7-121">Este parámetro puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="dccc7-121">This parameter can be NULL.</span></span> <span data-ttu-id="dccc7-122">Si este parámetro no es NULL, el miembro **objectname** de la estructura a la que apunta el parámetro *OBJECTATTRIBUTES* debe ser null.</span><span class="sxs-lookup"><span data-stu-id="dccc7-122">If this parameter is not NULL, the **ObjectName** member of the structure pointed to by the *ObjectAttributes* parameter must be NULL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dccc7-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dccc7-123">Return value</span></span>

<span data-ttu-id="dccc7-124">Devuelve un código de error **NTSTATUS** o.</span><span class="sxs-lookup"><span data-stu-id="dccc7-124">Returns an **NTSTATUS** or error code.</span></span>

<span data-ttu-id="dccc7-125">Los formularios y la importancia de los códigos de error de **NTSTATUS** se enumeran en el archivo de encabezado NTSTATUS. h disponible en el WDK y se describen en la documentación de WDK.</span><span class="sxs-lookup"><span data-stu-id="dccc7-125">The forms and significance of **NTSTATUS** error codes are listed in the Ntstatus.h header file available in the WDK, and are described in the WDK documentation.</span></span>

## <a name="remarks"></a><span data-ttu-id="dccc7-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dccc7-126">Remarks</span></span>

<span data-ttu-id="dccc7-127">Esta función no tiene ningún archivo de encabezado asociado.</span><span class="sxs-lookup"><span data-stu-id="dccc7-127">This function has no associated header file.</span></span> <span data-ttu-id="dccc7-128">La biblioteca de importación asociada, ntdll. lib, está disponible en el WDK.</span><span class="sxs-lookup"><span data-stu-id="dccc7-128">The associated import library, Ntdll.lib is available in the WDK.</span></span> <span data-ttu-id="dccc7-129">También puede utilizar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Ntdll.dll.</span><span class="sxs-lookup"><span data-stu-id="dccc7-129">You can also use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="dccc7-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dccc7-130">Requirements</span></span>



| <span data-ttu-id="dccc7-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="dccc7-131">Requirement</span></span> | <span data-ttu-id="dccc7-132">Value</span><span class="sxs-lookup"><span data-stu-id="dccc7-132">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="dccc7-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dccc7-133">DLL</span></span><br/> | <dl> <span data-ttu-id="dccc7-134"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dccc7-134"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
