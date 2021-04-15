---
description: 'Revise el texto del proveedor de forma más exhaustiva que ISpellCheckProvider:: check.'
ms.assetid: BD334EB8-4E14-478D-AB2A-E7F863C4BE0F
title: 'IComprehensiveSpellCheckProvider:: ComprehensiveCheck (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IComprehensiveSpellCheckProvider.ComprehensiveCheck
api_type:
- COM
api_location:
- spellcheckprovider.h
ms.openlocfilehash: d999a90166e0d54d537abc84c30f6c4e0ee3768c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688709"
---
# <a name="icomprehensivespellcheckprovidercomprehensivecheck-method"></a><span data-ttu-id="a188f-103">IComprehensiveSpellCheckProvider:: ComprehensiveCheck (método)</span><span class="sxs-lookup"><span data-stu-id="a188f-103">IComprehensiveSpellCheckProvider::ComprehensiveCheck method</span></span>

<span data-ttu-id="a188f-104">Revise el texto del proveedor de forma más exhaustiva que [**ISpellCheckProvider:: Check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check).</span><span class="sxs-lookup"><span data-stu-id="a188f-104">Spell-check the provider text in a more thorough manner than [**ISpellCheckProvider::Check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check).</span></span>

## <a name="syntax"></a><span data-ttu-id="a188f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a188f-105">Syntax</span></span>


```C++
HRESULT ComprehensiveCheck(
  [in]  PCWSTR             text,
  [out] IEnumSpellingError **result
);
```



## <a name="parameters"></a><span data-ttu-id="a188f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a188f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a188f-107">*texto* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="a188f-107">*text* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a188f-108">Texto que se va a comprobar.</span><span class="sxs-lookup"><span data-stu-id="a188f-108">The text to check.</span></span>

</dd> <dt>

<span data-ttu-id="a188f-109">*resultado* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a188f-109">*result* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a188f-110">Resultado de la comprobación de este texto, como una enumeración de errores ortográficos ([**IEnumSpellingError**](/windows/desktop/api/Spellcheck/nn-spellcheck-ienumspellingerror)), si existe.</span><span class="sxs-lookup"><span data-stu-id="a188f-110">The result of checking this text, as an enumeration of spelling errors ([**IEnumSpellingError**](/windows/desktop/api/Spellcheck/nn-spellcheck-ienumspellingerror)), if any.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a188f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a188f-111">Return value</span></span>

<span data-ttu-id="a188f-112">Este método puede devolver uno de estos valores.</span><span class="sxs-lookup"><span data-stu-id="a188f-112">This method can return one of these values.</span></span>



| <span data-ttu-id="a188f-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a188f-113">Return value</span></span>                                                                             | <span data-ttu-id="a188f-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="a188f-114">Description</span></span>                           |
|------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="a188f-115"><dt>S \_ correcto</dt></span><span class="sxs-lookup"><span data-stu-id="a188f-115"><dt>S\_OK</dt></span></span> </dl>         | <span data-ttu-id="a188f-116">Ejecutado.</span><span class="sxs-lookup"><span data-stu-id="a188f-116">Successful.</span></span><br/>                |
| <dl> <span data-ttu-id="a188f-117"><dt>E \_ INVALIDARG</dt></span><span class="sxs-lookup"><span data-stu-id="a188f-117"><dt>E\_INVALIDARG</dt></span></span> </dl> | <span data-ttu-id="a188f-118">el *texto* es una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="a188f-118">*text* is an empty string.</span></span><br/> |
| <dl> <span data-ttu-id="a188f-119"><dt>\_puntero E</dt></span><span class="sxs-lookup"><span data-stu-id="a188f-119"><dt>E\_POINTER</dt></span></span> </dl>    | <span data-ttu-id="a188f-120">el *texto* es un puntero nulo.</span><span class="sxs-lookup"><span data-stu-id="a188f-120">*text* is a null pointer.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="a188f-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a188f-121">Remarks</span></span>

<span data-ttu-id="a188f-122">No es necesario que la interfaz la implemente un proveedor de revisión ortográfica.</span><span class="sxs-lookup"><span data-stu-id="a188f-122">This interface isn't required to be implemented by a spell check provider.</span></span> <span data-ttu-id="a188f-123">Pero si el proveedor admite dos "modos" de revisión ortográfica (más rápido y más lento, pero más exhaustivo), debe implementar esta interfaz en el mismo objeto que implementa [**ISpellCheckProvider**](/windows/desktop/api/Spellcheckprovider/nn-spellcheckprovider-ispellcheckprovider) para admitir el modo de comprobación más exhaustivo.</span><span class="sxs-lookup"><span data-stu-id="a188f-123">But if the provider supports two "modes" of spell checking (a faster one and a slower but more thorough one), it should implement this interface in the same object that implements [**ISpellCheckProvider**](/windows/desktop/api/Spellcheckprovider/nn-spellcheckprovider-ispellcheckprovider) to support the more thorough checking mode.</span></span> <span data-ttu-id="a188f-124">Cuando un cliente llama a [**elemento:: ComprehensiveCheck**](/windows/desktop/api/Spellcheck/nf-spellcheck-ispellchecker-comprehensivecheck), la funcionalidad de revisión ortográfica ejecutará [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en el proveedor de [**IComprehensiveSpellCheckProvider**](/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-icomprehensivespellcheckprovider)y llamará a **IComprehensiveSpellCheckProvider. ComprehensiveCheck** si se admite la interfaz.</span><span class="sxs-lookup"><span data-stu-id="a188f-124">When a client calls [**ISpellChecker::ComprehensiveCheck**](/windows/desktop/api/Spellcheck/nf-spellcheck-ispellchecker-comprehensivecheck), the spell checking functionality will [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) the provider for [**IComprehensiveSpellCheckProvider**](/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-icomprehensivespellcheckprovider), and call **IComprehensiveSpellCheckProvider.ComprehensiveCheck** if the interface is supported.</span></span> <span data-ttu-id="a188f-125">Si no se admite la interfaz, se revertirá a [**ISpellCheckProvider:: Check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check).</span><span class="sxs-lookup"><span data-stu-id="a188f-125">If the interface isn't supported, it will silently fall back to [**ISpellCheckProvider::Check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check).</span></span>

## <a name="see-also"></a><span data-ttu-id="a188f-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="a188f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a188f-127">**IComprehensiveSpellCheckProvider**</span><span class="sxs-lookup"><span data-stu-id="a188f-127">**IComprehensiveSpellCheckProvider**</span></span>](/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-icomprehensivespellcheckprovider)
</dt> <dt>

[<span data-ttu-id="a188f-128">**IEnumSpellingError**</span><span class="sxs-lookup"><span data-stu-id="a188f-128">**IEnumSpellingError**</span></span>](/windows/desktop/api/Spellcheck/nn-spellcheck-ienumspellingerror)
</dt> <dt>

[<span data-ttu-id="a188f-129">**Elemento:: ComprehensiveCheck**</span><span class="sxs-lookup"><span data-stu-id="a188f-129">**ISpellChecker::ComprehensiveCheck**</span></span>](/windows/desktop/api/Spellcheck/nf-spellcheck-ispellchecker-comprehensivecheck)
</dt> <dt>

[<span data-ttu-id="a188f-130">**ISpellCheckProvider**</span><span class="sxs-lookup"><span data-stu-id="a188f-130">**ISpellCheckProvider**</span></span>](/windows/desktop/api/Spellcheckprovider/nn-spellcheckprovider-ispellcheckprovider)
</dt> <dt>

[<span data-ttu-id="a188f-131">**ISpellCheckProvider:: check**</span><span class="sxs-lookup"><span data-stu-id="a188f-131">**ISpellCheckProvider::Check**</span></span>](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check)
</dt> </dl>

 

 
