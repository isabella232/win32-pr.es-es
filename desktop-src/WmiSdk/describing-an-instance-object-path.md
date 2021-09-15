---
description: Una ruta de acceso de objeto de instancia describe la ubicación de una instancia de una clase determinada dentro de un espacio de nombres específico.
ms.assetid: 78a194f0-cd21-4622-9242-be7e430b96c0
ms.tgt_platform: multiple
title: Descripción de una ruta de acceso de objeto de instancia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f977359ea9c3c4346052f1edd076c0cce5544441
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467272"
---
# <a name="describing-an-instance-object-path"></a>Descripción de una ruta de acceso de objeto de instancia

Una ruta de acceso de objeto de instancia describe la ubicación de una instancia de una clase determinada dentro de un espacio de nombres específico.

Puede tener varios tipos diferentes de rutas de acceso de objeto de instancia:

-   Completo

    Una ruta de acceso de objeto de instancia completa anexa el nombre y el valor de la propiedad key de la clase a una ruta de acceso de objeto de clase completa.

    En el ejemplo siguiente se muestra la definición de la ruta de acceso completa del objeto de instancia.

    ``` syntax
    \\Server\Namespace:Class.KeyName="KeyValue"
    ```

-   Relativo

    Una ruta de acceso de objeto relativa hace referencia a una instancia ubicada en el espacio de nombres actual en el servidor actual. La ruta de acceso relativa consta del nombre de clase seguido de los nombres y valores de las propiedades de clave de esta instancia.

    En el ejemplo siguiente se muestra la definición de la ruta de acceso del objeto de instancia relativa.

    ``` syntax
    MyClass.MyProp="e:"
    ```

-   Relativo con una sola clave

    Para las clases con una sola propiedad designada como clave, puede omitir el nombre de la propiedad de clave.

    En el ejemplo siguiente se muestra la definición de la ruta de acceso del objeto de instancia relativa con una sola clave.

    ``` syntax
    MyClass="e:"
    ```

-   Relativo con varias claves

    Use una coma para distinguir entre las claves de una instancia con varias claves.

    En el ejemplo siguiente se muestran las definiciones de la ruta de acceso del objeto de instancia relativa con varias claves.

    ``` syntax
    MyOtherClass.FirstKey=1,SecondKey=2
    ```

-   Relativa para una clase singleton

    La ruta de acceso de objeto relativa para una clase singleton consta del nombre de clase seguido de la notación "=@".

    En el ejemplo siguiente se muestra la definición de la ruta de acceso del objeto de instancia relativa para una clase singleton.

    ``` syntax
    MySingletonClass=@
    ```

En el procedimiento siguiente se describe cómo recuperar una instancia de clase.

**Para recuperar una instancia de clase**

1.  Inicialice una cadena que contenga la ruta de acceso del objeto con una llamada a la [**función SysAllocString.**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring)
2.  Inicialice un objeto que recibirá la instancia de .
3.  Recupere el objeto con una llamada a [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) o [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).

    Para usar [**GetObjectAsync,**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)debe implementar la [**interfaz IWbemSink.**](swbemsink.md)

La siguiente instrucción include es necesaria para que el código que se muestra más \# adelante en este tema se compile correctamente.


```C++
#include <wbemidl.h>
```



En el ejemplo de código siguiente se describe cómo recuperar una instancia de clase mediante una ruta de acceso de objeto.


```C++
IWbemServices* pWbemSvcs = 0;

BSTR Path = SysAllocString(L"ComPort=2");    
IWbemClassObject *pComPort = 0;
pWbemSvcs->GetObject(Path, 0, 0, &pComPort, 0);
```



Para las instancias de clases que especifican varias propiedades como clave, WMI no requiere ninguna ordenación específica de las propiedades de clave en las rutas de acceso de objeto. Solo debe especificar el valor de cada una de las propiedades en la ruta de acceso del objeto.

En el ejemplo de código siguiente se describen dos descripciones de clave equivalentes.

``` syntax
MyClass.IntVal=33,StrVal="AAA"
MyClass.StrVal="AAA",IntVal=33
```

 

 
