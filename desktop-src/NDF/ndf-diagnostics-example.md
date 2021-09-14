---
title: Ejemplo de diagnóstico de NDF
description: En el ejemplo siguiente se muestra cómo iniciar la interfaz de usuario de NDF y diagnosticar la conectividad con el sitio web http //www.microsoft.com.
ms.assetid: 6fe3af13-7216-4ac9-91ac-c497d25521ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75fca4d54519988c3182b50a7c304f9c76a86392
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161200"
---
# <a name="ndf-diagnostics-example"></a>Ejemplo de diagnóstico de NDF

En el ejemplo siguiente se muestra cómo iniciar la interfaz de usuario de NDF y diagnosticar la conectividad con el sitio web https://www.microsoft.com .


```C++
#include "ndfapi.h"

NDFHANDLE hNDF;
HRESULT hr = NdfCreateWebIncident (
                    L"https://www.microsoft.com",
                    &hNDF);

if(SUCCEEDED(hr))
{
    NdfExecuteDiagnosis(hNDF, NULL); // launches the NDF UI
                                     // the UI is not modal to the original window
    NdfCloseIncident(hNDF);
}
```



La interfaz de usuario de NDF se puede iniciar como una ventana modal. Para ello, cambie el segundo parámetro de [**NdfExecuteDiagdiag de**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfexecutediagnosis) **NULL** al identificador (HWND) de la ventana primaria.

Este ejemplo se puede modificar para diagnosticar otras áreas de redes. Para ello, reemplace la llamada [**NdfCreateWebIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincident) por una de las otras funciones de creación de incidentes, como [**NdfCreateDNSIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatednsincident) o [**NdfCreateWinSockIncident.**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewinsockincident)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**NdfCloseIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcloseincident)
</dt> <dt>

[**NdfCreateWebIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincident)
</dt> <dt>

[**NdfExecuteDiagdiagdiag**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfexecutediagnosis)
</dt> </dl>

 

 




