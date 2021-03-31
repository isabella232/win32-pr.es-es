---
description: El siguiente procedimiento proporciona una breve introducción al proceso de compilación.
ms.assetid: a369d4d7-bd4b-4b4d-846e-ad85251e9ffb
title: Compilar un comando de APDU ISO7816-4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63987f27e74dd30b4520e6e09f27ae716d793d40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275798"
---
# <a name="building-an-iso7816-4-apdu-command"></a>Compilar un comando de APDU ISO7816-4

Para agregar funcionalidad a un proveedor de servicios, debe saber cómo se crea una [*unidad de datos de protocolo de aplicación*](/windows/desktop/SecGloss/a-gly) ISO7816-4 (APDU) dentro de los archivos DLL del proveedor de servicios base. El siguiente procedimiento proporciona una breve introducción al proceso de compilación.

> [!Note]  
> El ejemplo que se incluye aquí no es necesariamente completo; para obtener más información, vea las aplicaciones de ejemplo y los archivos dll.

 

**Para compilar un comando de APDU ISO7816-4**

1.  Cree un objeto [**ISCardCmd**](iscardcmd.md) y un objeto [**ISCardISO7816**](iscardiso7816.md) .

    ```C++
    //  Create an ISCardCmd object.
    HRESULT hresult = CoCreateInstance(CLSID_CSCardCmd,
                               NULL,
                               CLSCTX_ALL,
                               IID_ISCardCmd,
                               (LPVOID*) &g_pISCardCmd);
    //  Create an ISCardISO7816 object.
    HRESULT hresult = CoCreateInstance(CLSID_CSCardISO7816,
                               NULL,
                               CLSCTX_ALL,
                               IID_ISCardISO7816,
                               (LPVOID*) &g_pISCardISO7816);
    ```

    

    La interfaz [**ISCardCmd**](iscardcmd.md) contiene dos búferes **IByteBuffer** . Un búfer contiene la cadena de comando APDU real (además de los datos que se van a enviar con el comando). El otro contiene cualquier información de respuesta devuelta por la tarjeta después de la ejecución del comando.

2.  Con estos objetos, cree un comando ISO7816-4 válido como se indica a continuación:

    ```C++
    //  Do challenge.
    HRESULT hresult = g_pISCardISO7816->GetChallenge(dwLengthOfChallenge,
                                             &g_pISCardCmd);
    ```

    

    Este es el código que se usa en el método [**GetChallenge**](iscardiso7816-getchallenge.md) :

    ```C++
    #include <windows.h>

    STDMETHODIMP CSCardISO7816::GetChallenge(IN DWORD dwBytesExpected /*= 0*/,
                                IN OUT LPSCARDCMD *ppCmd)
    {
        //  Locals.
        HRESULT hr = S_OK;
        
        try
        {
            //  Is the ISCardCmd object okay?
            hr = IsSCardCmdValid(ppCmd);
            if (FAILED(hr))
                throw (hr);

            //  Do it.
            hr = (*ppCmd)->BuildCmd(m_byClassId,
                                    (BYTE) INS_GET_CHALLENGE,
                                    (BYTE) INS_NULL,  // P1 = 0x00
                                    (BYTE) INS_NULL,  // P2 = 0x00
                                    NULL,
                                    &dwBytesExpected);
            if (FAILED(hr))
                throw (hr);
        }
    }
    ```

    

    El método [**ISCardISO7816:: GetChallenge**](iscardiso7816-getchallenge.md) usa el método [**ISCardCmd:: BuildCmd**](iscardcmd-buildcmd.md) para compilar las APDU solicitadas. Para ello, se escribe la información adecuada en el búfer APDU [**ISCardCmd**](iscardcmd.md) en la siguiente instrucción:

    ```C++
    hr = (*ppCmd)->BuildCmd;
    ```

    

3.  Con el objeto [**ISCardCmd**](iscardcmd.md) compilado, realice una transacción con la tarjeta, interprete los resultados y continúe.

## <a name="expanding-beyond-iso7816-4"></a>Expandir más allá de ISO7816-4

El método recomendado para expandir el proceso de compilación o ejecución del proveedor de servicios descrito anteriormente es crear un nuevo objeto COM. Este objeto COM debe admitir una nueva interfaz que permita la creación de comandos no ISO7816-4 y debe agregar la interfaz [**ISCardISO7816**](iscardiso7816.md) .

## <a name="example-of-building-an-iso7816-4-apdu-command"></a>Ejemplo de creación de un comando de APDU ISO7816-4

En el ejemplo siguiente se muestra el código utilizado en el procedimiento anterior.


```C++
//  Create an ISCardCmd object.
hresult = CoCreateInstance(CLSID_CSCardCmd,
                           NULL,
                           CLSCTX_ALL,
                           IID_ISCardCmd,
                           (LPVOID*) &g_pISCardCmd);
//  Create an ISCardISO7816 object.
hresult = CoCreateInstance(CLSID_CSCardISO7816,
                           NULL,
                           CLSCTX_ALL,
                           IID_ISCardISO7816,
                           (LPVOID*) &g_pISCardISO7816);
//  Do challenge.
hresult = g_pISCardISO7816->GetChallenge(dwLengthOfChallenge,
                                         &g_pISCardCmd);

STDMETHODIMP
CSCardISO7816::GetChallenge(IN DWORD dwBytesExpected /*= 0*/,
                            IN OUT LPSCARDCMD *ppCmd)
{
    //  Locals.
    HRESULT hr = S_OK;
    
    try
    {
        //  Is the ISCardCmd object okay?
        hr = IsSCardCmdValid(ppCmd);
        if (FAILED(hr))
            throw (hr);

        //  Do it.
        hr = (*ppCmd)->BuildCmd(m_byClassId,
                                (BYTE) INS_GET_CHALLENGE,
                                (BYTE) INS_NULL,  // P1 = 0x00
                                (BYTE) INS_NULL,  // P2 = 0x00
                                NULL,
                                &dwBytesExpected);
        if (FAILED(hr))
            throw (hr);
    }
}
```



 

 
