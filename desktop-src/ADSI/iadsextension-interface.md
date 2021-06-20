---
title: Interfaz IADsExtension
description: Este artículo contiene la definición de código de C++ de la interfaz IADsExtension y la explicación de sus métodos.
ms.assetid: fa94cc55-1ab2-4b6e-a3b6-8c20542adb42
ms.tgt_platform: multiple
keywords:
- IADsExtension ADSI ,using
- ADSI ADSI, código de ejemplo C/C++, mediante IADsExtension
- extensiones ADSI, IADsExtension
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae7d59048d29620cdc2d3703b9ba26a852441a47
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405948"
---
# <a name="iadsextension-interface"></a><span data-ttu-id="e6658-106">Interfaz IADsExtension</span><span class="sxs-lookup"><span data-stu-id="e6658-106">IADsExtension Interface</span></span>

<span data-ttu-id="e6658-107">La [**interfaz IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) se define de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="e6658-107">The [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) interface is defined as follows:</span></span>


```C++
IADsExtension : public IUnknown
    {
    public:
        virtual HRESULT STDMETHODCALLTYPE Operate( 
            /* [in] */ DWORD dwCode,
            /* [in] */ VARIANT varData1,
            /* [in] */ VARIANT varData2,
            /* [in] */ VARIANT varData3) = 0;
 
        virtual HRESULT STDMETHODCALLTYPE PrivateGetIDsOfNames( 
            /* [in] */ REFIID riid,
            /* [in] */ OLECHAR **rgszNames,
            /* [in] */ unsigned int cNames,
            /* [in] */ LCID lcid,
            /* [out] */ DISPID *rgDispid) = 0;
 
        virtual HRESULT STDMETHODCALLTYPE PrivateInvoke( 
            /* [in] */ DISPID dispidMember,
            /* [in] */ REFIID riid,
            /* [in] */ LCID lcid,
            /* [in] */ WORD wFlags,
            /* [in] */ DISPPARAMS *pdispparams,
            /* [out] */ VARIANT *pvarResult,
            /* [out] */ EXCEPINFO *pexcepinfo,
            /* [out] */ unsigned int *puArgErr) = 0;
    };
```



<span data-ttu-id="e6658-108">El agregador (ADSI) llama al [**método IADsExtension::Operate.**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate)</span><span class="sxs-lookup"><span data-stu-id="e6658-108">The aggregator (ADSI) calls the [**IADsExtension::Operate**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) method.</span></span> <span data-ttu-id="e6658-109">La extensión debe interpretar el *parámetro dwCode* y cada *parámetro varData,* según la documentación del proveedor.</span><span class="sxs-lookup"><span data-stu-id="e6658-109">The extension should interpret the *dwCode* parameter and each *varData* parameter, according to the provider's documentation.</span></span>

<span data-ttu-id="e6658-110">El agregador (ADSI) llama al [**método IADsExtension::P rivateGetIDsOfNames.**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames)</span><span class="sxs-lookup"><span data-stu-id="e6658-110">The aggregator (ADSI), calls the [**IADsExtension::PrivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) method.</span></span> <span data-ttu-id="e6658-111">Se llama después de que ADSI determine la extensión para dar servicio al envío.</span><span class="sxs-lookup"><span data-stu-id="e6658-111">It is called after ADSI determines the extension to service the dispatch.</span></span> <span data-ttu-id="e6658-112">La extensión podría usar la información de tipo para obtener DISPID, es decir, mediante la [**función DispGetIDsOfNames.**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-dispgetidsofnames)</span><span class="sxs-lookup"><span data-stu-id="e6658-112">The extension could use the type information for getting the DISPID, that is, using the [**DispGetIDsOfNames**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-dispgetidsofnames) function.</span></span>

<span data-ttu-id="e6658-113">ADSI normalmente llama al [**método PrivateInvoke después**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) de llamar a la [**función PrivateGetIDsOfNames.**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames)</span><span class="sxs-lookup"><span data-stu-id="e6658-113">ADSI normally calls the [**PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) method after calling the [**PrivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) function.</span></span> <span data-ttu-id="e6658-114">La extensión debe llamar al método real que implementa.</span><span class="sxs-lookup"><span data-stu-id="e6658-114">The extension should call the actual method that it implements.</span></span> <span data-ttu-id="e6658-115">Como alternativa, la extensión puede usar información de tipo y llamar a [**la función DispInvoke.**](/windows/win32/api/oleauto/nf-oleauto-dispinvoke)</span><span class="sxs-lookup"><span data-stu-id="e6658-115">Alternatively, the extension can use type information and call the [**DispInvoke**](/windows/win32/api/oleauto/nf-oleauto-dispinvoke) function.</span></span>

<span data-ttu-id="e6658-116">Todos los parámetros tienen el mismo significado que los parámetros del método [**estándar IDispatch::Invoke.**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke)</span><span class="sxs-lookup"><span data-stu-id="e6658-116">All parameters have the same meaning as the parameters in the standard [**IDispatch::Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) method.</span></span>

 

 