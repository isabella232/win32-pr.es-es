---
description: Las llamadas semisincronosas son los medios recomendados para llamar a métodos WMI, como IWbemServices::ExecMethod y métodos de proveedor, como el método Chkdsk de la clase \_ LogicalDisk win32.
ms.assetid: 3d5ddd77-19f7-42d0-b8ca-a0a11f6b3f0f
ms.tgt_platform: multiple
title: Realizar una llamada semisincronosa con C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4a550c5ad659ab9b640a1fcb3060b5f6cc7671f80c209d238cd859ad0ef6f49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050703"
---
# <a name="making-a-semisynchronous-call-with-c"></a>Realizar una llamada semisincronosa con C++

Las llamadas semisincronosas son los medios recomendados para llamar a métodos WMI, como [**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) y métodos de proveedor, como el método Chkdsk de la clase [**\_ LogicalDisk de Win32**](/windows/desktop/CIMWin32Prov/chkdsk-method-in-class-win32-logicaldisk).

Una desventaja del procesamiento sincrónico es que el subproceso del llamador se bloquea hasta que se completa la llamada. El bloqueo puede provocar un retraso en el tiempo de procesamiento. En cambio, una llamada asincrónica debe implementar [**SWbemSink en**](swbemsink.md) el script. En C++, el código asincrónico debe implementar la [**interfaz IWbemObjectSink,**](iwbemobjectsink.md) usar varios subprocesos y controlar el flujo de información al autor de la llamada. Los conjuntos de resultados grandes de las consultas, por ejemplo, pueden tardar una cantidad considerable de tiempo en entregarse y obligan al autor de la llamada a dedicar recursos significativos del sistema para controlar la entrega.

El procesamiento semisincronoso resuelve los problemas de bloqueo de subprocesos y entrega no controlada sondeando un objeto de estado especial que implementa la [**interfaz IWbemCallResult.**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult) A **través de IWbemCallResult,** puede mejorar la velocidad y la eficacia de las consultas, enumeraciones y notificaciones de eventos.

En el procedimiento siguiente se describe cómo realizar una llamada semisincronosa con la [**interfaz IWbemServices.**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)

**Para realizar una llamada semisincronosa con la interfaz IWbemServices**

1.  Haga que la llamada sea normal, pero con la marca **WBEM \_ FLAG RETURN \_ \_ IMMEDIATELY** establecida en el *parámetro IFlags.*

    Puede combinar **WBEM \_ FLAG RETURN \_ \_ IMMEDIATELY** con otras marcas que sean válidas para el método específico. Por ejemplo, use la marca **WBEM \_ FLAG FORWARD \_ \_ ONLY** para todas las llamadas que devuelven enumeradores. Establecer estas marcas en combinación ahorra tiempo y espacio, y mejora la capacidad de respuesta.

2.  Sondee los resultados.

    Si llama a un método que devuelve un enumerador, como [**IWbemServices::CreateClassEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum) o [**IWbemServices::ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery), puede sondear los enumeradores con los métodos [**IEnumWbemClassObject::Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) o [**IEnumWbemClassObject::NextAsync.**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-nextasync) La **llamada a IEnumWbemClassObject::NextAsync** no es de bloqueo y se devuelve inmediatamente. En segundo plano, WMI comienza a entregar el número solicitado de objetos mediante una llamada [**a IWbemObjectSink::Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate). A continuación, WMI se detiene y espera otra **llamada a NextAsync.**

    Si llama a un método que no devuelve un enumerador, como [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject), debe establecer el parámetro *ppCallResult* en un puntero válido. Use [**IWbemCallResult::GetCallStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getcallstatus) en el puntero devuelto para recuperar **WBEM \_ S NO \_ \_ ERROR**.

3.  Finalice la llamada.

    Para una llamada que devuelve un enumerador, WMI llama a [**IWbemObjectSink::SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) para notificar la finalización de la operación. Si no necesita el resultado completo, libere el enumerador mediante una llamada al [**método IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)::[**Release.**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) Al **llamar a Release,** WMI cancela la entrega de todos los objetos que permanecen.

    Para una llamada que no usa un enumerador, recupere el objeto [**GetCallStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getcallstatus) mediante el *parámetro plStatus* del método .

El ejemplo de código de C++ de este tema requiere que las siguientes \# instrucciones include se compilen correctamente.


```C++
#include <comdef.h>
#include <wbemidl.h>
```



En el ejemplo de código siguiente se muestra cómo realizar una llamada semisincronosa a [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).


```C++
void GetObjSemiSync(IWbemServices *pSvc)
{

    IWbemCallResult *pCallRes = 0;
    IWbemClassObject *pObj = 0;
    
    HRESULT hRes = pSvc->GetObject(_bstr_t(L"MyClass=\"AAA\""), 0,
        0, 0, &pCallRes
        );
        
    if (hRes || pCallRes == 0)
        return;
        
    while (true)
    {
        LONG lStatus = 0;
        HRESULT hRes = pCallRes->GetCallStatus(5000, &lStatus);
        if ( hRes == WBEM_S_NO_ERROR || hRes != WBEM_S_TIMEDOUT )
            break;

        // Do another task
    }

    hRes = pCallRes->GetResultObject(5000, &pObj);
    if (hRes)
    {
        pCallRes->Release();
        return;
    }

    pCallRes->Release();

    // Use the object.

    // ...

    // Release it.
    // ===========
        
    pObj->Release();    // Release objects not owned.            
  
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Llamar a un método](calling-a-method.md)
</dt> </dl>

 

 
