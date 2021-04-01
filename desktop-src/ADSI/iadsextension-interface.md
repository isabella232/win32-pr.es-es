---
title: Interfaz IADsExtension
description: Este tema contiene ejemplos de código de C++ para usar la interfaz IADsExtension.
ms.assetid: fa94cc55-1ab2-4b6e-a3b6-8c20542adb42
ms.tgt_platform: multiple
keywords:
- IADsExtension ADSI, usar
- ADSI ADSI, código de ejemplo C/C++, uso de IADsExtension
- extensiones ADSI, IADsExtension
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6c950b6d305cc4c90ed75ff0cc96b5f7f344e12
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793821"
---
# <a name="iadsextension-interface"></a>Interfaz IADsExtension

La interfaz [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) se define de la siguiente manera:


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



El agregador (ADSI) llama al método [**IADsExtension:: Operate**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) . La extensión debe interpretar el parámetro *dwCode* y cada parámetro *varData* , según la documentación del proveedor.

El agregador (ADSI) llama al método [**IADsExtension::P rivategetidsofnames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) . Se llama después de que ADSI determina la extensión para atender el envío. La extensión podría usar la información de tipo para obtener el DISPID, es decir, el uso de la función [**DispGetIDsOfNames**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-dispgetidsofnames) .

Normalmente, ADSI llama al método [**PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) después de llamar a la función [**PrivateGetIDsOfNames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) . La extensión debe llamar al método real que implementa. Como alternativa, la extensión puede usar la información de tipo y llamar a la función [**DispInvoke**](/windows/win32/api/oleauto/nf-oleauto-dispinvoke) .

Todos los parámetros tienen el mismo significado que los parámetros del método [**IDispatch:: Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) estándar.

 

 