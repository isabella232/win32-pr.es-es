---
description: El \_ método GetObjectText del objeto SWbemLastError devuelve una representación textual del objeto en un formato Managed Object Format (MOF).
ms.assetid: efe3f3f6-c2f2-4295-bbf3-60d5b06ef98f
ms.tgt_platform: multiple
title: Método SWbemLastError.GetObjectText_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError.GetObjectText_
- ISWbemLastError.GetObjectText_
- ISWbemLastError.GetObjectText_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4247b5212e453c2f4393c26cd5ad63f07992c75a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002121"
---
# <a name="swbemlasterrorgetobjecttext_-method"></a><span data-ttu-id="214da-103">SWbemLastError. GetObjectText, \_ método</span><span class="sxs-lookup"><span data-stu-id="214da-103">SWbemLastError.GetObjectText\_ method</span></span>

<span data-ttu-id="214da-104">El **método \_ GetObjectText** del objeto [**SWbemLastError**](swbemlasterror.md) devuelve una representación textual del objeto en un formato [Managed Object Format (MOF)](managed-object-format--mof-.md) .</span><span class="sxs-lookup"><span data-stu-id="214da-104">The **GetObjectText\_** method of the [**SWbemLastError**](swbemlasterror.md) object returns a textual rendering of the object in a [Managed Object Format (MOF)](managed-object-format--mof-.md) format.</span></span> <span data-ttu-id="214da-105">Este objeto MOF se puede usar para mostrar el contenido de un objeto.</span><span class="sxs-lookup"><span data-stu-id="214da-105">This MOF object can be used to display an object's contents.</span></span> <span data-ttu-id="214da-106">Observe que el texto MOF que se devuelve no contiene toda la información sobre el objeto, sino solo información suficiente para que el compilador MOF pueda volver a crear el objeto original.</span><span class="sxs-lookup"><span data-stu-id="214da-106">Notice that the MOF text that is returned does not contain all the information about the object, but only enough information for the MOF compiler to be able to re-create the original object.</span></span> <span data-ttu-id="214da-107">Por ejemplo, no encontrará información sobre los calificadores propagados o las propiedades de la clase primaria.</span><span class="sxs-lookup"><span data-stu-id="214da-107">For instance, you will not find any information about the propagated qualifiers or the parent class properties.</span></span>

<span data-ttu-id="214da-108">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="214da-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="214da-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="214da-109">Syntax</span></span>


```VB
strMofText = .GetObjectText_( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="214da-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="214da-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="214da-111">*iFlags* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="214da-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="214da-112">Este parámetro está reservado y debe ser 0 (cero) si se especifica.</span><span class="sxs-lookup"><span data-stu-id="214da-112">This parameter is reserved and must be 0 (zero) if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="214da-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="214da-113">Return value</span></span>

<span data-ttu-id="214da-114">Si es correcto, este método devuelve una cadena que contiene el texto de salida.</span><span class="sxs-lookup"><span data-stu-id="214da-114">If successful, this method returns a string that contains the output text.</span></span>

## <a name="error-codes"></a><span data-ttu-id="214da-115">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="214da-115">Error codes</span></span>

<span data-ttu-id="214da-116">Una vez finalizado el **método \_ GetObjectText** , el objeto **Err** puede contener uno de los códigos de error de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="214da-116">Upon the completion of the **GetObjectText\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="214da-117">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="214da-117">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="214da-118">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="214da-118">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="214da-119">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="214da-119">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="214da-120">Un parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="214da-120">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="214da-121">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="214da-121">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="214da-122">Memoria insuficiente para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="214da-122">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="214da-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="214da-123">Requirements</span></span>



| <span data-ttu-id="214da-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="214da-124">Requirement</span></span> | <span data-ttu-id="214da-125">Value</span><span class="sxs-lookup"><span data-stu-id="214da-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="214da-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="214da-126">Minimum supported client</span></span><br/> | <span data-ttu-id="214da-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="214da-127">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="214da-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="214da-128">Minimum supported server</span></span><br/> | <span data-ttu-id="214da-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="214da-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="214da-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="214da-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="214da-131"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="214da-131"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="214da-132">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="214da-132">Type library</span></span><br/>             | <dl> <span data-ttu-id="214da-133"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="214da-133"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="214da-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="214da-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="214da-135"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="214da-135"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="214da-136">CLSID</span><span class="sxs-lookup"><span data-stu-id="214da-136">CLSID</span></span><br/>                    | <span data-ttu-id="214da-137">CLSID \_ SWbemLastError</span><span class="sxs-lookup"><span data-stu-id="214da-137">CLSID\_SWbemLastError</span></span><br/>                                                        |
| <span data-ttu-id="214da-138">IID</span><span class="sxs-lookup"><span data-stu-id="214da-138">IID</span></span><br/>                      | <span data-ttu-id="214da-139">\_ISWBEMLASTERROR IID</span><span class="sxs-lookup"><span data-stu-id="214da-139">IID\_ISWbemLastError</span></span><br/>                                                         |



 

 




