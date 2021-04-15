---
description: 'Las llamadas semisincrónica son el medio recomendado para llamar a métodos WMI, como IWbemServices:: ExecMethod y métodos de proveedor, como el método CHKDSK de la \_ clase Win32 LogicalDisk.'
ms.assetid: 3d5ddd77-19f7-42d0-b8ca-a0a11f6b3f0f
ms.tgt_platform: multiple
title: Realización de una llamada semisincrónica con C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c4546a7220d191b822e9f0f30a767e89e4dc26a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546179"
---
# <a name="making-a-semisynchronous-call-with-c"></a>Realización de una llamada semisincrónica con C++

Las llamadas semisincrónica son el medio recomendado para llamar a métodos WMI, como [**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) y métodos de proveedor, como el [**método CHKDSK de la \_ clase Win32 LogicalDisk**](/windows/desktop/CIMWin32Prov/chkdsk-method-in-class-win32-logicaldisk).

Una desventaja del procesamiento sincrónico es que el subproceso del llamador se bloquea hasta que se completa la llamada. El bloqueo puede producir un retraso en el tiempo de procesamiento. En cambio, una llamada asincrónica debe implementar [**SWbemSink**](swbemsink.md) en el script. En C++, el código asincrónico debe implementar la interfaz [**IWbemObjectSink**](iwbemobjectsink.md) , usar varios subprocesos y controlar el flujo de información de vuelta al autor de la llamada. Los grandes conjuntos de resultados de las consultas, por ejemplo, pueden tardar una cantidad considerable de tiempo en entregar y obligar a que el autor de la llamada dedique bastantes recursos del sistema para controlar la entrega.

El procesamiento semisincrónico resuelve el bloqueo de subprocesos y los problemas de entrega no controlada mediante el sondeo de un objeto de estado especial que implementa la interfaz [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult) . A través de **IWbemCallResult**, puede mejorar la velocidad y la eficacia de las consultas, las enumeraciones y las notificaciones de eventos.

En el procedimiento siguiente se describe cómo crear una llamada semisincrónica con la interfaz [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .

**Para hacer una llamada semisincrónica con la interfaz IWbemServices**

1.  Realice la llamada de la forma habitual, pero con la **marca WBEM devolver la marca \_ \_ \_ inmediatamente** establecida en el parámetro *IFlags* .

    Puede combinar la **devolución de la marca WBEM de \_ \_ \_ inmediato** con otras marcas válidas para el método concreto. Por ejemplo, use la **marca \_ WBEM \_ marcar \_ solo hacia delante** para todas las llamadas que devuelven enumeradores. Si se establecen estas marcas en combinación, se ahorra tiempo y espacio, y mejora la capacidad de respuesta.

2.  Sondear los resultados.

    Si llama a un método que devuelve un enumerador, como [**IWbemServices:: CreateClassEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum) o [**IWbemServices:: ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery), puede sondear los enumeradores con los métodos [**IEnumWbemClassObject:: Next**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-next) o [**IEnumWbemClassObject:: NextAsync**](/windows/desktop/api/Wbemcli/nf-wbemcli-ienumwbemclassobject-nextasync) . La llamada a **IEnumWbemClassObject:: NextAsync** es de no bloqueo y vuelve inmediatamente. En segundo plano, WMI comienza a ofrecer el número solicitado de objetos mediante una llamada a [**IWbemObjectSink:: indica**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate). WMI se detiene entonces y espera otra llamada **NextAsync** .

    Si llama a un método que no devuelve un enumerador, como [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject), debe establecer el parámetro *ppCallResult* en un puntero válido. Use [**IWbemCallResult:: GetCallStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getcallstatus) en el puntero devuelto para recuperar **WBEM \_ S \_ no \_ error**.

3.  Finalice la llamada.

    En el caso de una llamada que devuelve un enumerador, WMI llama a [**IWbemObjectSink:: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) para notificar la finalización de la operación. Si no necesita todo el resultado, libere el enumerador llamando al método [**IEnumWbemClassObject**](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)::[**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) . La llamada a los resultados de la **versión** en WMI cancela la entrega de todos los objetos que permanecen.

    En el caso de una llamada que no use un enumerador, recupere el objeto [**GetCallStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemcallresult-getcallstatus) mediante el parámetro *plStatus* de su método.

El ejemplo de código de C++ de este tema requiere las siguientes \# instrucciones include para compilar correctamente.


```C++
#include <comdef.h>
#include <wbemidl.h>
```



En el ejemplo de código siguiente se muestra cómo hacer una llamada semisincrónica a [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).


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

 

 
