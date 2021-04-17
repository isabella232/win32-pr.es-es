---
description: Establece la lista de identificadores de grupo persistentes para todos los perfiles que se conservan en la aplicación.
ms.assetid: EF83F295-CD53-45A4-B209-560B4069CA7C
title: Función WFDDisplaySinkSetPersistedGroupIDList (Wfdsink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFDSetDisplaySinkPersistedGroupIDList
api_type:
- DllExport
api_location:
- wifidisplay.dll
ms.openlocfilehash: 423360d7127f331fd1aa2de7f7370daebcc2b417
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666793"
---
# <a name="wfddisplaysinksetpersistedgroupidlist-function"></a><span data-ttu-id="82eec-103">WFDDisplaySinkSetPersistedGroupIDList función)</span><span class="sxs-lookup"><span data-stu-id="82eec-103">WFDDisplaySinkSetPersistedGroupIDList function</span></span>

<span data-ttu-id="82eec-104">Establece la lista de identificadores de grupo persistentes para todos los perfiles que se conservan en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="82eec-104">Sets the persisted group id list for all the profiles that are persisted by your app.</span></span> <span data-ttu-id="82eec-105">La aplicación debe llamar a este método cada vez que agrega o elimina un perfil de su almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="82eec-105">Your app should call this method every time it adds or deletes a profile from its storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="82eec-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="82eec-106">Syntax</span></span>


```C++
DWORD WINAPI WFDSetDisplaySinkPersistedGroupIDList(
  _In_ UINT32             cGroupIDList,
  _In_ DOT11_WFD_GROUP_ID *pGroupIDList
);
```



## <a name="parameters"></a><span data-ttu-id="82eec-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="82eec-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82eec-108">*cGroupIDList* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="82eec-108">*cGroupIDList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82eec-109">Recuento de identificadores de grupo a los que apunta *pGroupIDList*.</span><span class="sxs-lookup"><span data-stu-id="82eec-109">The count of group ids being pointed to by *pGroupIDList*.</span></span>

</dd> <dt>

<span data-ttu-id="82eec-110">*pGroupIDList* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="82eec-110">*pGroupIDList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82eec-111">Puntero a una matriz de identificadores de grupo de *cGroupIDList* .</span><span class="sxs-lookup"><span data-stu-id="82eec-111">Pointer to an array of *cGroupIDList* group ids.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82eec-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="82eec-112">Return value</span></span>

<span data-ttu-id="82eec-113">Si la función se ejecuta correctamente, el valor devuelto es ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="82eec-113">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

## <a name="remarks"></a><span data-ttu-id="82eec-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="82eec-114">Remarks</span></span>

<span data-ttu-id="82eec-115">Siempre se espera que se llame a este método con toda la lista, no un subconjunto.</span><span class="sxs-lookup"><span data-stu-id="82eec-115">This method is always expected to be called with the entire list, and not a subset.</span></span> <span data-ttu-id="82eec-116">Es correcto llamar a este método con los perfiles 0 cuando el almacén de perfiles está vacío.</span><span class="sxs-lookup"><span data-stu-id="82eec-116">It is OK to call this method with 0 profiles when the profile store is empty.</span></span>

<span data-ttu-id="82eec-117">Se producirá un error al volver a invocar un identificador de grupo que no forma parte de la lista proporcionada. Grupo P2P desconocido "(estado 8).</span><span class="sxs-lookup"><span data-stu-id="82eec-117">A re-invoke for a group id that is not part of the provided list will fail with "Fail; unknown P2P Group"(status 8).</span></span>

## <a name="requirements"></a><span data-ttu-id="82eec-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82eec-118">Requirements</span></span>



| <span data-ttu-id="82eec-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="82eec-119">Requirement</span></span> | <span data-ttu-id="82eec-120">Value</span><span class="sxs-lookup"><span data-stu-id="82eec-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="82eec-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="82eec-121">Minimum supported client</span></span><br/> | <span data-ttu-id="82eec-122">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="82eec-122">Windows 8.1 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="82eec-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="82eec-123">Minimum supported server</span></span><br/> | <span data-ttu-id="82eec-124">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="82eec-124">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="82eec-125">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="82eec-125">End of client support</span></span><br/>    | <span data-ttu-id="82eec-126">Windows 10</span><span class="sxs-lookup"><span data-stu-id="82eec-126">Windows 10</span></span><br/>                                                                      |
| <span data-ttu-id="82eec-127">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="82eec-127">End of server support</span></span><br/>    | <span data-ttu-id="82eec-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="82eec-128">Windows Server 2016</span></span><br/>                                                             |
| <span data-ttu-id="82eec-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="82eec-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="82eec-130"><dt>Wfdsink. h</dt></span><span class="sxs-lookup"><span data-stu-id="82eec-130"><dt>Wfdsink.h</dt></span></span> </dl>       |
| <span data-ttu-id="82eec-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="82eec-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="82eec-132"><dt>Wifidisplay. lib</dt></span><span class="sxs-lookup"><span data-stu-id="82eec-132"><dt>Wifidisplay.lib</dt></span></span> </dl> |
| <span data-ttu-id="82eec-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="82eec-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82eec-134"><dt>Wifidisplay.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82eec-134"><dt>Wifidisplay.dll</dt></span></span> </dl> |



 

 




