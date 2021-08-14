---
title: Recuperar información sobre errores
description: Recuperar información sobre errores
ms.assetid: 51a0e401-43f2-4738-9799-a96e2580a29f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e26844505b7c5de3e39c3199a6087c94f35bed9f64ef11a65d1c6df9a3dd4e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118309657"
---
# <a name="retrieving-error-information"></a>Recuperar información sobre errores

Con las funciones y las interfaces de control de errores COM, puede recuperar la información de error como se muestra a continuación:

1.  Compruebe si el valor devuelto representa un error que el objeto está preparado para controlar.
2.  Llame [**a QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) para obtener un puntero a la [**interfaz ISupportErrorInfo.**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) A continuación, llame a [**ISupportErrorInfo::InterfaceSupportsErrorInfo**](/windows/win32/api/oaidl/nf-oaidl-isupporterrorinfo-interfacesupportserrorinfo) para comprobar que el error lo ha producido el objeto que lo devolvió y que el objeto de error pertenece al error actual y no a una llamada anterior.
3.  Para obtener un puntero al objeto de error, llame a [**la función GetErrorInfo.**](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo)
4.  Para recuperar información del objeto de error, use los [**métodos IErrorInfo.**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo)

Si el objeto no está preparado para controlar el error, pero necesita propagar la información de error más abajo en la cadena de llamadas, simplemente debe pasar el valor devuelto a su autor de la llamada. Dado que la función [**GetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo) borra la información de error y pasa la propiedad del objeto de error al autor de la llamada, solo debe llamar a la función el objeto que controla el error.

 

 