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
# <a name="iadsextension-interface"></a>Interfaz IADsExtension

La [**interfaz IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) se define de la siguiente manera:


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



El agregador (ADSI) llama al [**método IADsExtension::Operate.**](/windows/desktop/api/Iads/nf-iads-iadsextension-operate) La extensión debe interpretar el *parámetro dwCode* y cada *parámetro varData,* según la documentación del proveedor.

El agregador (ADSI) llama al [**método IADsExtension::P rivateGetIDsOfNames.**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) Se llama después de que ADSI determine la extensión para dar servicio al envío. La extensión podría usar la información de tipo para obtener DISPID, es decir, mediante la [**función DispGetIDsOfNames.**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-dispgetidsofnames)

ADSI normalmente llama al [**método PrivateInvoke después**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) de llamar a la [**función PrivateGetIDsOfNames.**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) La extensión debe llamar al método real que implementa. Como alternativa, la extensión puede usar información de tipo y llamar a [**la función DispInvoke.**](/windows/win32/api/oleauto/nf-oleauto-dispinvoke)

Todos los parámetros tienen el mismo significado que los parámetros del método [**estándar IDispatch::Invoke.**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke)

 

 