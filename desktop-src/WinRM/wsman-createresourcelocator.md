---
title: Método WSMan. CreateResourceLocator (WSManDisp. h)
description: Crea un objeto ResourceLocator que se puede usar en lugar de especificar un URI de recurso en operaciones de objeto de sesión como Session. get, Session. put o Session. Enumerate.
ms.assetid: 1b04fe11-ec90-4374-9838-a0df313b722e
ms.tgt_platform: multiple
keywords:
- Método CreateResourceLocator Administración remota de Windows
- Administración remota de Windows método CreateResourceLocator, objeto WSMan
- Administración remota de Windows de objeto WSMan, método CreateResourceLocator
topic_type:
- apiref
api_name:
- WSMan.CreateResourceLocator
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6982d1ea0b257ca9276918931ce233e675fd3eb3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996305"
---
# <a name="wsmancreateresourcelocator-method"></a><span data-ttu-id="ef599-106">WSMan. CreateResourceLocator (método)</span><span class="sxs-lookup"><span data-stu-id="ef599-106">WSMan.CreateResourceLocator method</span></span>

<span data-ttu-id="ef599-107">Crea un objeto [**ResourceLocator**](resourcelocator.md) que se puede usar en lugar de especificar un URI de recurso en operaciones de objeto de [**sesión**](session.md) como [**Session. Get**](session-get.md), [**Session. put**](session-put.md)o [**Session. Enumerate**](session-enumerate.md).</span><span class="sxs-lookup"><span data-stu-id="ef599-107">Creates a [**ResourceLocator**](resourcelocator.md) object that can be used instead of specifying a resource URI in [**Session**](session.md) object operations such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ef599-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ef599-108">Syntax</span></span>


```VB
WSMan.CreateResourceLocator( _
  [ ByVal uri ] _
)
```



## <a name="parameters"></a><span data-ttu-id="ef599-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ef599-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef599-110">*identificador URI* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="ef599-110">*uri* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ef599-111">El URI de recurso para el recurso.</span><span class="sxs-lookup"><span data-stu-id="ef599-111">The resource URI for the resource.</span></span> <span data-ttu-id="ef599-112">Para obtener más información sobre las cadenas URI, consulte [URI de recursos](resource-uris.md).</span><span class="sxs-lookup"><span data-stu-id="ef599-112">For more information about URI strings, see [Resource URIs](resource-uris.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef599-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ef599-113">Return value</span></span>

<span data-ttu-id="ef599-114">Un objeto [**ResourceLocator**](resourcelocator.md) que se puede usar para realizar operaciones WinRM locales o remotas.</span><span class="sxs-lookup"><span data-stu-id="ef599-114">A [**ResourceLocator**](resourcelocator.md) object that can then be used to perform local or remote WinRM operations.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef599-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ef599-115">Remarks</span></span>

<span data-ttu-id="ef599-116">Si no se especifica la propiedad **FragmentDialect** en el objeto [**ResourceLocator**](resourcelocator.md) , el valor predeterminado es la especificación XPath 1,0.</span><span class="sxs-lookup"><span data-stu-id="ef599-116">If the **FragmentDialect** property is not specified in the [**ResourceLocator**](resourcelocator.md) object, the default is the XPath 1.0 specification.</span></span> <span data-ttu-id="ef599-117">Para más información, consulte [https://www.w3.org/TR/xpath](https://www.w3.org/TR/xpath).</span><span class="sxs-lookup"><span data-stu-id="ef599-117">For more information, see [https://www.w3.org/TR/xpath](https://www.w3.org/TR/xpath).</span></span>

## <a name="examples"></a><span data-ttu-id="ef599-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ef599-118">Examples</span></span>

<span data-ttu-id="ef599-119">En el siguiente ejemplo de código de VBScript se crea un objeto [**ResourceLocator**](resourcelocator.md) y se obtiene el valor de la propiedad **Descripción** del adaptador de red de la instancia de [**Win32 \_ NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration) con un índice de "1".</span><span class="sxs-lookup"><span data-stu-id="ef599-119">The following VBScript code example creates a [**ResourceLocator**](resourcelocator.md) object and gets the network adapter **Description** property value from the instance of [**Win32\_NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration) with an Index of "1".</span></span>


```VB
const Uri = "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_NetworkAdapterConfiguration"
const FragmentPath = "Description"

Set objWSMan = CreateObject("WSMan.Automation")

Set objSession = objWSMan.CreateSession()

Set objLocator = objWSMan.CreateResourceLocator(Uri)

objLocator.AddSelector "Index", "1"
objLocator.FragmentPath = FragmentPath

Dim Xml
Xml = objSession.Get(objLocator)
WScript.Echo Xml
```



## <a name="requirements"></a><span data-ttu-id="ef599-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef599-120">Requirements</span></span>



| <span data-ttu-id="ef599-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef599-121">Requirement</span></span> | <span data-ttu-id="ef599-122">Value</span><span class="sxs-lookup"><span data-stu-id="ef599-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef599-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ef599-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ef599-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ef599-124">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="ef599-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ef599-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ef599-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ef599-126">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="ef599-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ef599-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef599-128"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef599-128"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ef599-129">IDL</span><span class="sxs-lookup"><span data-stu-id="ef599-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ef599-130"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ef599-130"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="ef599-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ef599-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="ef599-132"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ef599-132"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ef599-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ef599-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef599-134"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef599-134"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ef599-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="ef599-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef599-136">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="ef599-136">**WSMan**</span></span>](wsman.md)
</dt> <dt>

[<span data-ttu-id="ef599-137">**ConnectionOptions**</span><span class="sxs-lookup"><span data-stu-id="ef599-137">**ConnectionOptions**</span></span>](connectionoptions.md)
</dt> <dt>

[<span data-ttu-id="ef599-138">**De sesión**</span><span class="sxs-lookup"><span data-stu-id="ef599-138">**Session**</span></span>](session.md)
</dt> </dl>

 

