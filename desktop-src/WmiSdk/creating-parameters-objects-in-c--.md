---
description: 'Los métodos IWbemServices:: ExecMethod o ExecMethodAsync requieren la \_ \_ clase de sistema Parameters como contenedor en pInParams si el método que se está ejecutando tiene argumentos de entrada.'
ms.assetid: 17b72ceb-e730-4176-aa4d-189d0b6acc8b
ms.tgt_platform: multiple
title: Crear objetos de parámetros en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c200958f4ad00ced5455462e7a2909ac6a58cfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276265"
---
# <a name="creating-parameters-objects-in-c"></a>Crear objetos de parámetros en C++

Los métodos [**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) o [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) requieren la clase de sistema [**\_ \_ Parameters**](--parameters.md) como contenedor en *pInParams* si el método que se está ejecutando tiene argumentos de entrada.

En el procedimiento siguiente se describe cómo crear una instancia de la clase del sistema [**\_ \_ Parameters**](--parameters.md) para almacenar la información de parámetros.

**Para crear una instancia de \_ \_ parámetros**

1.  Determine la ruta de acceso de la clase que contiene la definición del método.
2.  Usar la ruta de acceso de clase y el puntero [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) pasados desde [**IWbemProviderInit:: Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize), llamar a [**IWbemClassObject:: GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) para recuperar las clases de parámetros de entrada y salida.

    El método [**GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) devuelve un puntero [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) para tener acceso a cada una de estas clases.

3.  Con el puntero [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) para la clase de salida, llame a [**IWbemClassObject:: SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) para crear una instancia de la clase.
4.  Rellene la instancia de la clase estableciendo las propiedades que corresponden a los valores de salida y, si hay un valor devuelto para el método, la propiedad [ReturnValue](creating-a-method.md) .
5.  Vuelva a pasar la instancia de [**\_ \_ parámetros**](--parameters.md) al llamador a través del método [**IWbemObjectSink:: indica**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) .

Una vez que un proveedor de métodos determina que los parámetros de entrada son correctos, el método al que apunta *strMethodName* podría seguir superándose o producir un error. Algunos proveedores de métodos generan un segundo subproceso para implementar el método, de modo que el éxito o el error real del método terminen en informar al llamador a través de [**IWbemObjectSink:: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus). Tenga en cuenta que **IWbemObjectSink:: SetStatus** no recibe el código de retorno del método de proveedor. Sin embargo, recibe el código de retorno del mecanismo de devolución de llamada real y solo es útil para comprobar que la llamada se produjo o que se produjo un error por motivos mecánicos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Llamar a un método](calling-a-method.md)
</dt> <dt>

[**IWbemCallResult::GetResultObject**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getresultobject)
</dt> <dt>

[**IWbemServices:: ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)
</dt> <dt>

[**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod)
</dt> </dl>

 

 



