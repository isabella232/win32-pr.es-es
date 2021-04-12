---
description: Una ruta de acceso del objeto de instancia describe la ubicación de una instancia de una clase determinada dentro de un espacio de nombres concreto.
ms.assetid: 78a194f0-cd21-4622-9242-be7e430b96c0
ms.tgt_platform: multiple
title: Describir una ruta de acceso al objeto de instancia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f977359ea9c3c4346052f1edd076c0cce5544441
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361008"
---
# <a name="describing-an-instance-object-path"></a><span data-ttu-id="4cacb-103">Describir una ruta de acceso al objeto de instancia</span><span class="sxs-lookup"><span data-stu-id="4cacb-103">Describing an Instance Object Path</span></span>

<span data-ttu-id="4cacb-104">Una ruta de acceso del objeto de instancia describe la ubicación de una instancia de una clase determinada dentro de un espacio de nombres concreto.</span><span class="sxs-lookup"><span data-stu-id="4cacb-104">An instance object path describes the location of an instance of a given class within a specific namespace.</span></span>

<span data-ttu-id="4cacb-105">Puede tener varios tipos diferentes de rutas de acceso a objetos de instancia:</span><span class="sxs-lookup"><span data-stu-id="4cacb-105">You can have several different kinds of instance object paths:</span></span>

-   <span data-ttu-id="4cacb-106">Completo</span><span class="sxs-lookup"><span data-stu-id="4cacb-106">Full</span></span>

    <span data-ttu-id="4cacb-107">Una ruta de acceso al objeto de instancia completa anexa el nombre y el valor de la propiedad clave de la clase a una ruta de acceso de objeto de clase completa.</span><span class="sxs-lookup"><span data-stu-id="4cacb-107">A full instance object path appends the name and value of the key property for the class to a full class object path.</span></span>

    <span data-ttu-id="4cacb-108">En el ejemplo siguiente se muestra la definición de la ruta de acceso del objeto de instancia completa.</span><span class="sxs-lookup"><span data-stu-id="4cacb-108">The following example shows the definition of the full instance object path.</span></span>

    ``` syntax
    \\Server\Namespace:Class.KeyName="KeyValue"
    ```

-   <span data-ttu-id="4cacb-109">Relativo</span><span class="sxs-lookup"><span data-stu-id="4cacb-109">Relative</span></span>

    <span data-ttu-id="4cacb-110">Una ruta de acceso relativa del objeto hace referencia a una instancia ubicada en el espacio de nombres actual en el servidor actual.</span><span class="sxs-lookup"><span data-stu-id="4cacb-110">A relative object path refers to an instance located in the current namespace on the current server.</span></span> <span data-ttu-id="4cacb-111">La ruta de acceso relativa consta del nombre de clase seguido de los nombres y valores de las propiedades de clave de esta instancia.</span><span class="sxs-lookup"><span data-stu-id="4cacb-111">The relative path consists of the class name followed by the names and values of the key properties of this instance.</span></span>

    <span data-ttu-id="4cacb-112">En el ejemplo siguiente se muestra la definición de la ruta de acceso del objeto de instancia relativa.</span><span class="sxs-lookup"><span data-stu-id="4cacb-112">The following example shows the definition of the relative instance object path.</span></span>

    ``` syntax
    MyClass.MyProp="e:"
    ```

-   <span data-ttu-id="4cacb-113">Relativo a una sola clave</span><span class="sxs-lookup"><span data-stu-id="4cacb-113">Relative with a single key</span></span>

    <span data-ttu-id="4cacb-114">En el caso de las clases con una sola propiedad designada como clave, puede omitir el nombre de la propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="4cacb-114">For classes with only one property designated as the key, you can omit the name of the key property.</span></span>

    <span data-ttu-id="4cacb-115">En el ejemplo siguiente se muestra la definición de la ruta de acceso del objeto de instancia relativa con una sola clave.</span><span class="sxs-lookup"><span data-stu-id="4cacb-115">The following example shows the definition of the relative instance object path with a single key.</span></span>

    ``` syntax
    MyClass="e:"
    ```

-   <span data-ttu-id="4cacb-116">Relativo con varias claves</span><span class="sxs-lookup"><span data-stu-id="4cacb-116">Relative with multiple keys</span></span>

    <span data-ttu-id="4cacb-117">Use una coma para distinguir entre las claves de una instancia con varias claves.</span><span class="sxs-lookup"><span data-stu-id="4cacb-117">Use a comma to distinguish between the keys of an instance with multiple keys.</span></span>

    <span data-ttu-id="4cacb-118">En el siguiente ejemplo se muestran las definiciones de la ruta de acceso del objeto de instancia relativa con varias claves.</span><span class="sxs-lookup"><span data-stu-id="4cacb-118">The following example shows the definitions of the relative instance object path with multiple keys.</span></span>

    ``` syntax
    MyOtherClass.FirstKey=1,SecondKey=2
    ```

-   <span data-ttu-id="4cacb-119">Relativa para una clase singleton</span><span class="sxs-lookup"><span data-stu-id="4cacb-119">Relative for a singleton class</span></span>

    <span data-ttu-id="4cacb-120">La ruta de acceso relativa del objeto para una clase singleton está formada por el nombre de la clase seguido de la notación "= @".</span><span class="sxs-lookup"><span data-stu-id="4cacb-120">The relative object path for a singleton class consists of the class name followed by the "=@" notation.</span></span>

    <span data-ttu-id="4cacb-121">En el ejemplo siguiente se muestra la definición de la ruta de acceso del objeto de instancia relativa para una clase singleton.</span><span class="sxs-lookup"><span data-stu-id="4cacb-121">The following example shows the definition of the relative instance object path for a singleton class.</span></span>

    ``` syntax
    MySingletonClass=@
    ```

<span data-ttu-id="4cacb-122">En el procedimiento siguiente se describe cómo recuperar una instancia de clase.</span><span class="sxs-lookup"><span data-stu-id="4cacb-122">The following procedure describes how to retrieve a class instance.</span></span>

<span data-ttu-id="4cacb-123">**Para recuperar una instancia de clase**</span><span class="sxs-lookup"><span data-stu-id="4cacb-123">**To retrieve a class instance**</span></span>

1.  <span data-ttu-id="4cacb-124">Inicialice una cadena que contenga la ruta de acceso del objeto con una llamada a la función [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) .</span><span class="sxs-lookup"><span data-stu-id="4cacb-124">Initialize a string that contains the object path with a call to the [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) function.</span></span>
2.  <span data-ttu-id="4cacb-125">Inicialice un objeto que recibirá la instancia.</span><span class="sxs-lookup"><span data-stu-id="4cacb-125">Initialize an object that will receive the instance.</span></span>
3.  <span data-ttu-id="4cacb-126">Recupere el objeto con una llamada a [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) o [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="4cacb-126">Retrieve the object with a call to [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

    <span data-ttu-id="4cacb-127">Para usar [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync), debe implementar la interfaz [**IWbemSink**](swbemsink.md) .</span><span class="sxs-lookup"><span data-stu-id="4cacb-127">To use [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync), you must implement the [**IWbemSink**](swbemsink.md) interface.</span></span>

<span data-ttu-id="4cacb-128">La siguiente \# instrucción include es necesaria para que el código que se muestra más adelante en este tema se compile correctamente.</span><span class="sxs-lookup"><span data-stu-id="4cacb-128">The following \#include statement is required for the code that is listed later in this topic to compile correctly.</span></span>


```C++
#include <wbemidl.h>
```



<span data-ttu-id="4cacb-129">En el ejemplo de código siguiente se describe cómo recuperar una instancia de clase mediante una ruta de acceso de objeto.</span><span class="sxs-lookup"><span data-stu-id="4cacb-129">The following code example describes how to retrieve a class instance using an object path.</span></span>


```C++
IWbemServices* pWbemSvcs = 0;

BSTR Path = SysAllocString(L"ComPort=2");    
IWbemClassObject *pComPort = 0;
pWbemSvcs->GetObject(Path, 0, 0, &pComPort, 0);
```



<span data-ttu-id="4cacb-130">En el caso de las instancias de clases que especifican varias propiedades como clave, WMI no requiere un orden específico de propiedades clave en las rutas de acceso a objetos.</span><span class="sxs-lookup"><span data-stu-id="4cacb-130">For instances of classes that specify multiple properties as the key, WMI requires no specific ordering of key properties in object paths.</span></span> <span data-ttu-id="4cacb-131">Solo es necesario especificar el valor de cada una de las propiedades de la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="4cacb-131">You need only specify the value of each of the properties in the object path.</span></span>

<span data-ttu-id="4cacb-132">En el ejemplo de código siguiente se describen dos descripciones de clave equivalentes.</span><span class="sxs-lookup"><span data-stu-id="4cacb-132">The following code example describes two equivalent key descriptions.</span></span>

``` syntax
MyClass.IntVal=33,StrVal="AAA"
MyClass.StrVal="AAA",IntVal=33
```

 

 
