---
description: En el procedimiento siguiente se proporciona una breve introducción al proceso de compilación.
ms.assetid: a369d4d7-bd4b-4b4d-846e-ad85251e9ffb
title: Creación de un comando APDU ISO7816-4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 411e8c6957269c68f10ed3c62b95104ef893dd02206e22becf6227b59b12e37b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141298"
---
# <a name="building-an-iso7816-4-apdu-command"></a>Creación de un comando APDU ISO7816-4

Para agregar funcionalidad a un proveedor de servicios, debe saber cómo [](/windows/desktop/SecGloss/a-gly) se ha creado una unidad de datos del protocolo de aplicación (APDU) ISO7816-4 dentro de los archivos DLL del proveedor de servicios base. En el procedimiento siguiente se proporciona una breve introducción al proceso de compilación.

> [!Note]  
> El ejemplo que se incluye aquí no está necesariamente completo; Para obtener más información, vea las aplicaciones de ejemplo y los archivos DLL.

 

**Para compilar un comando DE APDU ISO7816-4**

1.  Cree un [**objeto ISCardCmd**](iscardcmd.md) y un [**objeto ISCardISO7816.**](iscardiso7816.md)

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

    

    La [**interfaz ISCardCmd**](iscardcmd.md) contiene dos búferes **IByteBuffer.** Un búfer contiene la cadena de comando de APDU real (además de los datos que se enviarán con el comando ). El otro contiene cualquier información de respuesta devuelta por la tarjeta después de la ejecución del comando.

2.  Con estos objetos, cree un comando ISO7816-4 válido como se muestra a continuación:

    ```C++
    //  Do challenge.
    HRESULT hresult = g_pISCardISO7816->GetChallenge(dwLengthOfChallenge,
                                             &g_pISCardCmd);
    ```

    

    Este es el código que se usa en [**el método GetChallenge:**](iscardiso7816-getchallenge.md)

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

    

    El [**método ISCardISO7816::GetChallenge**](iscardiso7816-getchallenge.md) usa el método [**ISCardCmd::BuildCmd**](iscardcmd-buildcmd.md) para compilar la APDU solicitada. Para ello, escriba la información adecuada en el búfer [**DE ISCardCmd**](iscardcmd.md) APDU en la instrucción siguiente:

    ```C++
    hr = (*ppCmd)->BuildCmd;
    ```

    

3.  Con el objeto [**ISCardCmd**](iscardcmd.md) creado, realice una transacción con la tarjeta, interprete los resultados y continúe.

## <a name="expanding-beyond-iso7816-4"></a>Expansión más allá de ISO7816-4

La manera recomendada de expandir el proceso de compilación o ejecución del proveedor de servicios descrito anteriormente es crear un nuevo objeto COM. Este objeto COM debe admitir una nueva interfaz que permita la creación de comandos que no son ISO7816-4 y debe agregar la [**interfaz ISCardISO7816.**](iscardiso7816.md)

## <a name="example-of-building-an-iso7816-4-apdu-command"></a>Ejemplo de creación de un comando APDU ISO7816-4

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



 

 
