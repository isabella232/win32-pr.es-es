---
description: La interfaz IWbemObjectSink crea una interfaz receptora que puede recibir todos los tipos de notificaciones dentro del modelo de programación WMI.
ms.assetid: 987aea1d-912a-4691-987f-181c1ef1a8a9
ms.tgt_platform: multiple
title: Interfaz IWbemObjectSink (Wbemcli.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemObjectSink
api_type:
- COM
api_location:
- Fastprox.dll
ms.openlocfilehash: 6bfce21edca92c95276f382d16007f8b319b9f3b80fc5c3c721f7232ea0b4618
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996545"
---
# <a name="iwbemobjectsink-interface"></a>Interfaz IWbemObjectSink

La **interfaz IWbemObjectSink** crea una interfaz receptora que puede recibir todos los tipos de notificaciones dentro del modelo de programación WMI. Los clientes deben implementar esta interfaz [](making-an-asynchronous-call-with-c--.md) para recibir los resultados de los [**métodos asincrónicos de IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)y tipos específicos de notificaciones de eventos. Los proveedores usan, pero no implementan esta interfaz para proporcionar eventos y objetos a WMI.

Normalmente, los proveedores llaman a una implementación proporcionada por WMI. En estos casos, llame a [**Indicar**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) para proporcionar objetos al servicio WMI. Después, llame a [**SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) para indicar el final de la secuencia de notificación. También puede llamar a **SetStatus para** indicar errores cuando el receptor no tiene ningún objeto.

Al programar clientes asincrónicos de WMI, el usuario proporciona la implementación. WMI llama a los métodos para entregar objetos y establecer el estado del resultado.

> [!Note]  
> Si una aplicación cliente pasa la misma interfaz receptora en dos llamadas asincrónicas superpuestas diferentes, WMI no garantiza el orden de la devolución de llamada. Las aplicaciones cliente que realicen llamadas asincrónicas superpuestas deben pasar objetos receptores diferentes o serializar sus llamadas.

 

> [!Note]  
> Dado que es posible que la llamada al receptor no se devuelva en el mismo nivel de autenticación que requiere el cliente, se recomienda usar la comunicación semisincronosa en lugar de la comunicación asincrónica. Para obtener más información, vea [Llamar a un método](calling-a-method.md).

 

## <a name="members"></a>Miembros

La **interfaz IWbemObjectSink** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IWbemObjectSink** tiene estos métodos.



| Método                                         | Descripción                                                                                                             |
|:-----------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**Indicar**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate)   | Recibe objetos de notificación.<br/>                                                                               |
| [**SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) | Lo llaman los orígenes para indicar el final de una secuencia de notificación o para enviar otros códigos de estado al receptor.<br/> |



 

## <a name="remarks"></a>Comentarios

Al implementar un receptor de suscripción de eventos (**IWbemObjectSink** o [**IWbemEventSink**](iwbemeventsink.md)), no llame a WMI desde los métodos [**Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) o [**SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) del objeto receptor. Por ejemplo, llamar a [**IWbemServices::CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) para cancelar el receptor desde dentro de una implementación de [**Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) puede interferir con el estado wmi. Para cancelar una suscripción de eventos, establezca una marca y llame a **IWbemServices::CancelAsyncCall** desde otro subproceso u objeto. Para las implementaciones que no están relacionadas con un receptor de eventos, como recuperaciones de objetos, enumeraciones y consultas, puede volver a llamar a WMI.

Las implementaciones de receptor deben procesar la notificación de eventos en un plazo de 100 MSEC porque el subproceso WMI que entrega la notificación de eventos no puede realizar otro trabajo hasta que el objeto receptor haya completado el procesamiento. Si la notificación requiere una gran cantidad de procesamiento, el receptor puede usar una cola interna para que otro subproceso controle el procesamiento.

## <a name="examples"></a>Ejemplos

El ejemplo de código siguiente es una implementación simple de un receptor de objetos. Este ejemplo se puede usar con [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) o [**IWbemServices::CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) para recibir las instancias devueltas:


```C++
#include <iostream>
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")

class QuerySink : public IWbemObjectSink
{
    LONG m_lRef;
    bool bDone; 

public:
    QuerySink() { m_lRef = 0; }
   ~QuerySink() { bDone = TRUE; }

    virtual ULONG STDMETHODCALLTYPE AddRef();
    virtual ULONG STDMETHODCALLTYPE Release();        
    virtual HRESULT STDMETHODCALLTYPE 
        QueryInterface(REFIID riid, void** ppv);

    virtual HRESULT STDMETHODCALLTYPE Indicate( 
            /* [in] */
            LONG lObjectCount,
            /* [size_is][in] */
            IWbemClassObject __RPC_FAR *__RPC_FAR *apObjArray
            );
        
    virtual HRESULT STDMETHODCALLTYPE SetStatus( 
            /* [in] */ LONG lFlags,
            /* [in] */ HRESULT hResult,
            /* [in] */ BSTR strParam,
            /* [in] */ IWbemClassObject __RPC_FAR *pObjParam
            );
};


ULONG QuerySink::AddRef()
{
    return InterlockedIncrement(&m_lRef);
}

ULONG QuerySink::Release()
{
    LONG lRef = InterlockedDecrement(&m_lRef);
    if(lRef == 0)
        delete this;
    return lRef;
}

HRESULT QuerySink::QueryInterface(REFIID riid, void** ppv)
{
    if (riid == IID_IUnknown || riid == IID_IWbemObjectSink)
    {
        *ppv = (IWbemObjectSink *) this;
        AddRef();
        return WBEM_S_NO_ERROR;
    }
    else return E_NOINTERFACE;
}


HRESULT QuerySink::Indicate(long lObjCount, IWbemClassObject **pArray)
{
    for (long i = 0; i < lObjCount; i++)
    {
        IWbemClassObject *pObj = pArray[i];

        // ... use the object.

        // AddRef() is only required if the object will be held after
        // the return to the caller.
    }

    return WBEM_S_NO_ERROR;
}

HRESULT QuerySink::SetStatus(
            /* [in] */ LONG lFlags,
            /* [in] */ HRESULT hResult,
            /* [in] */ BSTR strParam,
            /* [in] */ IWbemClassObject __RPC_FAR *pObjParam
        )
{
    printf("QuerySink::SetStatus hResult = 0x%X\n", hResult);
    return WBEM_S_NO_ERROR;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                           |
| Header<br/>                   | <dl> <dt>Wbemcli.h (incluir Wbemidl.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Wbemuuid.lib</dt> </dl>                  |
| Archivo DLL<br/>                      | <dl> <dt>Fastprox.dll</dt> </dl>                  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[API COM para WMI](com-api-for-wmi.md)
</dt> <dt>

[Realizar una llamada asincrónica con C++](making-an-asynchronous-call-with-c--.md)
</dt> <dt>

[Establecer la seguridad en una llamada asincrónica](setting-security-on-an-asynchronous-call.md)
</dt> <dt>

[Recepción de eventos durante la duración de la aplicación](receiving-events-for-the-duration-of-your-application.md)
</dt> </dl>

 

 




