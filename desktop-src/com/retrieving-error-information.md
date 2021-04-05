---
title: Recuperar información sobre errores
description: Recuperar información sobre errores
ms.assetid: 51a0e401-43f2-4738-9799-a96e2580a29f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6a5918ee7338d1b8428079da20ecb43c7b4b4ef
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078399"
---
# <a name="retrieving-error-information"></a>Recuperar información sobre errores

Mediante las interfaces y funciones de control de errores COM, puede recuperar la información de error de la siguiente manera:

1.  Compruebe si el valor devuelto representa un error que el objeto está preparado para controlar.
2.  Llame a [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) para obtener un puntero a la interfaz [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) . A continuación, llame a [**ISupportErrorInfo:: InterfaceSupportsErrorInfo**](/windows/win32/api/oaidl/nf-oaidl-isupporterrorinfo-interfacesupportserrorinfo) para comprobar que el error lo ha producido el objeto que lo devolvió y que el objeto de error pertenece al error actual y no a una llamada anterior.
3.  Para obtener un puntero al objeto de error, llame a la función [**GetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo) .
4.  Para recuperar información del objeto de error, use los métodos [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) .

Si el objeto no está preparado para controlar el error, pero necesita propagar la información de error más abajo en la cadena de llamadas, simplemente debe pasar el valor devuelto a su llamador. Dado que la función [**GetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo) borra la información de error y pasa la propiedad del objeto de error al autor de la llamada, solo el objeto que controla el error debe llamar a la función.

 

 