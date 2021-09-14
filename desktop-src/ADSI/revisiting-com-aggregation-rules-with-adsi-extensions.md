---
title: Revisión de las reglas de agregación COM con extensiones ADSI
description: A continuación se muestra una breve revisión de las reglas de extensión ADSI y agregación COM.
ms.assetid: 3efcdfcf-4965-4436-90b2-dc0f627c71b4
ms.tgt_platform: multiple
keywords:
- Extensiones ADSI, reglas de agregación COM
- ADSI de agregación COM
- Revisión de las reglas de agregación COM con adsi extensions ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e9b3e3614c4adc225883f120f8fbf362df3e646
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172177"
---
# <a name="revisiting-com-aggregation-rules-with-adsi-extensions"></a>Revisión de las reglas de agregación COM con extensiones ADSI

A continuación se muestra una breve revisión de las reglas de extensión ADSI y agregación COM.

-   El **método CreateInstance** devuelve un puntero a una interfaz [**IUnknown,**](/windows/win32/api/unknwn/nn-unknwn-iunknown) como se indica a continuación, que no delega ninguna llamada de función al agregador.

    El [**método IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) devuelve punteros a las interfaces que admite y errores para las interfaces que no admite.

    El [**método IUnknown::AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) incrementa el recuento de referencias en el propio objeto de extensión agregado.

    El [**método IUnperin::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) disminuye el recuento de referencias en el propio objeto de extensión agregado y se destruye cuando el recuento de referencias es 0.

-   El objeto de extensión debe almacenar el puntero [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) del agregador, como m pOuterUnknown, durante la implementación del \_ **método CreateInstance.**
-   Todas las interfaces que admite el objeto de extensión, incluido [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension), deben heredar de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), que delega todas las llamadas de función al agregador.
    -   [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) llama a "m \_ pOuterUnknown->QueryInterface"
    -   [**IUnknown::AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) llama a "m \_ pOuterUnknown->AddRef"
    -   [**IUnldan::Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) llama a "m \_ pOuterUnknown->Release"

Los escritores de extensiones pueden elegir cualquier implementación interna que prefieran siempre que cumplan las reglas de agregación COM estándar. Tenga en cuenta que un objeto de extensión no tiene que funcionar como un objeto independiente. Las extensiones están diseñadas para funcionar como agregados. Sin embargo, se puede escribir una extensión para que funcione como un objeto independiente y como agregado.

Además de la compatibilidad con agregaciones COM estándar, un objeto de extensión puede admitir [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) para características más avanzadas. Si se admite el enlace en tiempo de tarde, la extensión debe:

-   Delegue las [**funciones para IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) de nuevo en el agregador.
-   Implemente [**la interfaz IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) [**en IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension).

 

 