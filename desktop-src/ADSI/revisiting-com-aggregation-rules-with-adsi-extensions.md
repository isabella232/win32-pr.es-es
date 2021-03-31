---
title: Revisar las reglas de agregación COM con extensiones ADSI
description: La siguiente es una breve revisión de las reglas de agregación de COM y de extensión ADSI.
ms.assetid: 3efcdfcf-4965-4436-90b2-dc0f627c71b4
ms.tgt_platform: multiple
keywords:
- Extensiones ADSI, reglas de agregación COM
- Agregación de COM ADSI
- Revisar las reglas de agregación COM con ADSI Extensions ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e9b3e3614c4adc225883f120f8fbf362df3e646
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793845"
---
# <a name="revisiting-com-aggregation-rules-with-adsi-extensions"></a>Revisar las reglas de agregación COM con extensiones ADSI

La siguiente es una breve revisión de las reglas de agregación de COM y de extensión ADSI.

-   El método **CreateInstance** devuelve un puntero a una interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) , como se indica a continuación, que no delega ninguna llamada de función al agregador.

    El método [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) devuelve punteros a las interfaces que admite y errores para las interfaces que no admite.

    El método [**IUnknown:: AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) incrementa el recuento de referencias en el propio objeto de extensión agregado.

    El método [**IUnkown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) reduce el recuento de referencias en el propio objeto de extensión agregado y se destruye cuando el recuento de referencias es 0.

-   El objeto de extensión debe almacenar el puntero [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) del agregador, como m \_ pOuterUnknown, durante la implementación del método **CreateInstance** .
-   Todas las interfaces que admite el objeto de extensión, incluido [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension), deben heredar de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), que delega de nuevo todas las llamadas de función al agregador.
    -   [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) llama a "m \_ POuterUnknown->QueryInterface"
    -   [**IUnknown:: AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) llama a "m \_ POuterUnknown->AddRef"
    -   [**IUnkown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) llama a "m \_ POuterUnknown->versión"

Los escritores de extensiones pueden elegir cualquier implementación interna que prefieran, siempre y cuando cumplan las reglas de agregación COM estándar. Tenga en cuenta que no es necesario que un objeto de extensión funcione como un objeto independiente. Las extensiones están diseñadas para funcionar como agregados. Sin embargo, se puede escribir una extensión para que funcione como un objeto independiente y como agregado.

Además de la compatibilidad con la agregación COM estándar, un objeto de extensión puede admitir [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension) para las características más avanzadas. Si se admite el enlace en tiempo de ejecución, la extensión debe:

-   Delegar funciones para [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) de nuevo al agregador.
-   Implemente la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) en [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension).

 

 