---
description: Abre un volumen especificado e inicializa su objeto de control de cuota.
ms.assetid: 20eae2a3-f602-48a2-bf1c-65570e7a5d21
title: DiskQuotaControl.Inimétodo tialize
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.Initialize
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 919720f01c67b6df3189b760aa8cefbb29615179
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984247"
---
# <a name="diskquotacontrolinitialize-method"></a><span data-ttu-id="d0b2f-103">DiskQuotaControl.Inimétodo tialize</span><span class="sxs-lookup"><span data-stu-id="d0b2f-103">DiskQuotaControl.Initialize method</span></span>

<span data-ttu-id="d0b2f-104">Abre un volumen especificado e inicializa su objeto de control de cuota.</span><span class="sxs-lookup"><span data-stu-id="d0b2f-104">Opens a specified volume and initializes its quota control object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0b2f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d0b2f-105">Syntax</span></span>


```JScript
DiskQuotaControl.Initialize(
  sPath,
  bReadWrite
)
```



## <a name="parameters"></a><span data-ttu-id="d0b2f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d0b2f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0b2f-107">*sPath*</span><span class="sxs-lookup"><span data-stu-id="d0b2f-107">*sPath*</span></span> 
</dt> <dd>

<span data-ttu-id="d0b2f-108">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="d0b2f-108">Type: **String**</span></span>

<span data-ttu-id="d0b2f-109">Valor de cadena que contiene la ruta de acceso completa del volumen que se va a inicializar.</span><span class="sxs-lookup"><span data-stu-id="d0b2f-109">A string value that contains the fully qualified path of the volume to be initialized.</span></span>

</dd> <dt>

<span data-ttu-id="d0b2f-110">*bReadWrite*</span><span class="sxs-lookup"><span data-stu-id="d0b2f-110">*bReadWrite*</span></span> 
</dt> <dd>

<span data-ttu-id="d0b2f-111">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="d0b2f-111">Type: **Boolean**</span></span>

<span data-ttu-id="d0b2f-112">Valor booleano que especifica cómo se va a abrir el volumen.</span><span class="sxs-lookup"><span data-stu-id="d0b2f-112">A Boolean value that specifies how the volume is to be opened.</span></span> <span data-ttu-id="d0b2f-113">Establezca *bReadWrite* en **true** para el acceso de lectura y escritura o **false** para el acceso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d0b2f-113">Set *bReadWrite* to **TRUE** for read/write access or **FALSE** for read-only access.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0b2f-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d0b2f-114">Return value</span></span>

<span data-ttu-id="d0b2f-115">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="d0b2f-115">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0b2f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0b2f-116">Requirements</span></span>



| <span data-ttu-id="d0b2f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0b2f-117">Requirement</span></span> | <span data-ttu-id="d0b2f-118">Value</span><span class="sxs-lookup"><span data-stu-id="d0b2f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0b2f-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0b2f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d0b2f-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d0b2f-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d0b2f-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0b2f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d0b2f-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d0b2f-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="d0b2f-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d0b2f-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0b2f-124"><dt>Shell32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="d0b2f-124"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0b2f-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="d0b2f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0b2f-126">**Objeto DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="d0b2f-126">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




