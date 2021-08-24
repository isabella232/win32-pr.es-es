---
description: Los métodos IWbemServices::ExecMethod o ExecMethodAsync requieren la clase del sistema PARAMETERS como contenedor en \_ pInParams si el método que están ejecutando tiene argumentos de \_ entrada.
ms.assetid: 17b72ceb-e730-4176-aa4d-189d0b6acc8b
ms.tgt_platform: multiple
title: Crear objetos de parámetros en C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaa97753eab9554e402a91cfce72a6435d44298b6b68a83de96fd4beccd83bd3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119244525"
---
# <a name="creating-parameters-objects-in-c"></a>Crear objetos de parámetros en C++

Los [**métodos IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) o [**ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) requieren la clase del sistema [**\_ \_ PARAMETERS**](--parameters.md) como contenedor en *pInParams* si el método que están ejecutando tiene argumentos de entrada.

En el procedimiento siguiente se describe cómo crear una instancia de la clase del sistema [**\_ \_ PARAMETERS**](--parameters.md) para contener información de parámetros.

**Para crear una instancia de \_ \_ PARAMETERS**

1.  Determine la ruta de acceso de clase para la clase que contiene la definición del método.
2.  Mediante la ruta de acceso de clase y el puntero [**IWbemServices pasados**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) desde [**IWbemProviderInit::Initialize**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemproviderinit-initialize), llame a [**IWbemClassObject::GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) para recuperar las clases de parámetros de entrada y salida.

    El [**método GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) devuelve un [**puntero IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) para tener acceso a cada una de estas clases.

3.  Mediante el [**puntero IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) para la clase de salida, llame a [**IWbemClassObject::SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) para crear una instancia de la clase .
4.  Rellene la instancia de clase estableciendo las propiedades correspondientes a los valores de salida y, si hay un valor devuelto para el método, la [propiedad ReturnValue.](creating-a-method.md)
5.  Vuelva a [**\_ \_ pasar la instancia PARAMETERS**](--parameters.md) al autor de la llamada mediante el método [**IWbemObjectSink::Indicate.**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate)

Después de que un proveedor de métodos determine que los parámetros de entrada son correctos, es posible que el método al que apunta *strMethodName* todavía pase o se pueda producir un error. Algunos proveedores de métodos generan un segundo subproceso para implementar el método de modo que el error o el éxito real del método terminen notificando al autor de la llamada a través de [**IWbemObjectSink::SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus). Tenga en **cuenta que IWbemObjectSink::SetStatus** no recibe el código de retorno del método de proveedor. Sin embargo, recibe el código de retorno del mecanismo de devolución de llamadas real y solo es útil para comprobar que la llamada se produjo o que se produjo un error por motivos mecánicos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Llamar a un método](calling-a-method.md)
</dt> <dt>

[**IWbemCallResult::GetResultObject**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getresultobject)
</dt> <dt>

[**IWbemServices::ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)
</dt> <dt>

[**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod)
</dt> </dl>

 

 



