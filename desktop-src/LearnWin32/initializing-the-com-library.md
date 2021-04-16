---
title: Inicializar la biblioteca COM
description: Inicializar la biblioteca COM
ms.assetid: b044e146-8409-4f8d-87d3-52f21ebc2255
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 663cfb73455e118579f45710788ab72385ada335
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105676378"
---
# <a name="initializing-the-com-library"></a>Inicializar la biblioteca COM

Cualquier programa de Windows que use COM debe inicializar la biblioteca COM mediante una llamada a la función [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) . Cada subproceso que usa una interfaz COM debe hacer una llamada independiente a esta función. **CoInitializeEx** tiene la firma siguiente:


```C++
HRESULT CoInitializeEx(LPVOID pvReserved, DWORD dwCoInit);
```



El primer parámetro está reservado y debe ser **null**. El segundo parámetro especifica el modelo de subprocesos que utilizará el programa. COM admite dos modelos de subprocesos diferentes, *Apartamento* y *multiproceso*. Si especifica el subprocesamiento de apartamento, está realizando las siguientes garantías:

-   Tendrá acceso a cada objeto COM desde un único subproceso; no se compartirán punteros de interfaz COM entre varios subprocesos.
-   El subproceso tendrá un bucle de mensajes. (Consulte [mensajes de ventana](window-messages.md) en el módulo 1).

Si alguna de estas restricciones no es true, utilice el modelo multiproceso. Para especificar el modelo de subprocesos, establezca una de las marcas siguientes en el parámetro *dwCoInit* .



| Marca                          | Descripción         |
|-------------------------------|---------------------|
| **APARTMENTTHREADED de coinit \_** | Subproceso de apartamento. |
| **multiproceso de coinit \_**     | Multiproceso.      |



 

Debe establecer exactamente una de estas marcas. Normalmente, un subproceso que crea una ventana debe usar la marca **\_ APARTMENTTHREADED de coinit** y otros subprocesos deben usar **coinit \_ multithreaded**. Sin embargo, algunos componentes COM requieren un modelo de subprocesos determinado. La documentación de MSDN le indicará cuándo es así.

> [!Note]  
> En realidad, incluso si se especifica el subprocesamiento de apartamento, todavía es posible compartir interfaces entre subprocesos mediante una técnica denominada *serialización*. El cálculo de referencias está fuera del ámbito de este módulo. Lo importante es que con el subprocesamiento de apartamento, nunca debe copiar simplemente un puntero de interfaz a otro subproceso. Para obtener más información sobre los modelos de subprocesos COM, consulte [procesos, subprocesos y apartamentos](/windows/desktop/com/processes--threads--and-apartments).

 

Además de las marcas ya mencionadas, es una buena idea establecer la marca de **\_ \_ OLE1DDE deshabilitar coinit** en el parámetro *dwCoInit* . La configuración de esta marca evita la sobrecarga asociada con la vinculación e incrustación de objetos (OLE) 1,0, una tecnología obsoleta.

Aquí se muestra cómo inicializar COM para el subprocesamiento de apartamento:


```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE);
```



El tipo de valor devuelto **HRESULT** contiene un error o código de operación correcta. Veremos el control de errores COM en la sección siguiente.

## <a name="uninitializing-the-com-library"></a>Anular la inicialización de la biblioteca COM

Para cada llamada correcta a [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex), debe llamar a [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) antes de que se cierre el subproceso. Esta función no toma ningún parámetro y no tiene ningún valor devuelto.


```C++
CoUninitialize();
```



## <a name="next"></a>Siguientes

[Códigos de error en COM](error-codes-in-com.md)

 

 