---
description: Establecimiento del registro de errores
ms.assetid: 2e3124e3-32d0-4eb6-9c1d-91b625018ac4
title: Establecimiento del registro de errores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5d28c337d146927ee624dad6f350d163e4bde3756acaf6fb0418821cc7ac5c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904205"
---
# <a name="setting-the-error-log"></a>Establecimiento del registro de errores

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

Después de implementar la clase de registro de errores, cree una nueva instancia de la clase . A continuación, DirectShow [Editing Services](directshow-editing-services.md) un puntero a él mediante una llamada al método [**IAMSetErrorLog::p ut \_ ErrorLog**](iamseterrorlog-put-errorlog.md) en la escala de tiempo. Consulte la escala de tiempo de **la interfaz IAMSetErrorLog.** Para asegurarse de que se registran todos los errores, debe llamar a este método antes de cargar, guardar o representar la escala de tiempo.


```C++
IAMSetErrorLog  *pSetLog = NULL;
IAMErrorLog     *pLog = new CErrReporter();

pTL->QueryInterface(IID_IAMSetErrorLog, (void **)&pSetLog);
pSetLog->put_ErrorLog(pLog);
pSetLog->Release();
```



El registro de errores no tiene ningún efecto en los valores devueltos que recibe al llamar a métodos en la aplicación. El registro de errores complementa, pero no reemplaza las técnicas habituales de control de errores. Para crear una aplicación sólida, compruebe siempre los valores HRESULT.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Errores de registro](logging-errors.md)
</dt> </dl>

 

 



