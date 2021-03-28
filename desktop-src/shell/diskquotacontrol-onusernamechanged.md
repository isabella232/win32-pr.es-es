---
description: Se produce cuando se ha resuelto la información de nombre de un objeto DIDiskQuotaUser.
ms.assetid: df32cb17-ad90-4535-a36b-60c5b4e9999f
title: Función OnUserNameChanged (dskquota. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OnUserNameChanged
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 98906f281c6c93a64754c1aa5cecfc6624599c40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360886"
---
# <a name="onusernamechanged-function"></a><span data-ttu-id="bad61-103">OnUserNameChanged función)</span><span class="sxs-lookup"><span data-stu-id="bad61-103">OnUserNameChanged function</span></span>

<span data-ttu-id="bad61-104">Se produce cuando se ha resuelto la información de nombre de un objeto [**DIDiskQuotaUser**](didiskquotauser-object.md) .</span><span class="sxs-lookup"><span data-stu-id="bad61-104">Occurs when the name information for a [**DIDiskQuotaUser**](didiskquotauser-object.md) object has been resolved.</span></span>

## <a name="parameters"></a><span data-ttu-id="bad61-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bad61-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bad61-106">*oUser*</span><span class="sxs-lookup"><span data-stu-id="bad61-106">*oUser*</span></span> 
</dt> <dd>

<span data-ttu-id="bad61-107">**Objeto** que se evalúa como el objeto [**DIDiskQuotaUser**](didiskquotauser-object.md) asociado al usuario cuyo nombre se ha resuelto.</span><span class="sxs-lookup"><span data-stu-id="bad61-107">The **Object** that evaluates to the [**DIDiskQuotaUser**](didiskquotauser-object.md) object associated with the user whose name has been resolved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bad61-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bad61-108">Return value</span></span>

<span data-ttu-id="bad61-109">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="bad61-109">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bad61-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bad61-110">Remarks</span></span>

<span data-ttu-id="bad61-111">Cuando un cliente [**enumera usuarios**](didiskquotauser-object.md)o llama al método [**adduser**](diskquotacontrol-adduser.md) o [**FindUser**](diskquotacontrol-finduser.md) , el nombre de usuario debe resolverse en el identificador de seguridad (SID) asociado.</span><span class="sxs-lookup"><span data-stu-id="bad61-111">When a client [**enumerates users**](didiskquotauser-object.md), or calls the [**AddUser**](diskquotacontrol-adduser.md) or [**FindUser**](diskquotacontrol-finduser.md) method, the user name must be resolved to the associated security ID (SID).</span></span> <span data-ttu-id="bad61-112">Dado que este procedimiento puede llevar mucho tiempo, un cliente puede tener una resolución de nombres realizada de forma asincrónica en un subproceso en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="bad61-112">Because this procedure can be time-consuming, a client can have name resolution done asynchronously on a background thread.</span></span> <span data-ttu-id="bad61-113">Cuando se resuelve el nombre de un usuario, el objeto [**DiskQuotaControl**](diskquotacontrol-object.md) notifica a su cliente desencadenando el evento **OnUserNameChanged** .</span><span class="sxs-lookup"><span data-stu-id="bad61-113">When a user's name is resolved, the [**DiskQuotaControl**](diskquotacontrol-object.md) object notifies its client by firing the **OnUserNameChanged** event.</span></span> <span data-ttu-id="bad61-114">Un objeto **DIDiskQuotaUser** asociado al usuario se pasa como un parámetro.</span><span class="sxs-lookup"><span data-stu-id="bad61-114">A **DIDiskQuotaUser** object associated with the user is passed as a parameter.</span></span> <span data-ttu-id="bad61-115">Este objeto permite al cliente modificar la configuración de la cuota del usuario.</span><span class="sxs-lookup"><span data-stu-id="bad61-115">This object allows the client to modify the user's quota settings.</span></span>

## <a name="requirements"></a><span data-ttu-id="bad61-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bad61-116">Requirements</span></span>



| <span data-ttu-id="bad61-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="bad61-117">Requirement</span></span> | <span data-ttu-id="bad61-118">Value</span><span class="sxs-lookup"><span data-stu-id="bad61-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bad61-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bad61-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bad61-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="bad61-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bad61-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bad61-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bad61-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bad61-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="bad61-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bad61-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="bad61-124"><dt>Dskquota. h</dt></span><span class="sxs-lookup"><span data-stu-id="bad61-124"><dt>Dskquota.h</dt></span></span> </dl>                         |
| <span data-ttu-id="bad61-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bad61-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bad61-126"><dt>Shell32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="bad61-126"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bad61-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="bad61-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bad61-128">**Objeto DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="bad61-128">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




