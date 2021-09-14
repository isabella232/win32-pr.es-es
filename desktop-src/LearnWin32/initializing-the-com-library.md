---
title: Inicialización de la biblioteca COM
description: Inicialización de la biblioteca COM
ms.assetid: b044e146-8409-4f8d-87d3-52f21ebc2255
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 663cfb73455e118579f45710788ab72385ada335
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159977"
---
# <a name="initializing-the-com-library"></a>Inicialización de la biblioteca COM

Cualquier Windows que use COM debe inicializar la biblioteca COM llamando a la [**función CoInitializeEx.**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) Cada subproceso que usa una interfaz COM debe realizar una llamada independiente a esta función. **CoInitializeEx** tiene la firma siguiente:


```C++
HRESULT CoInitializeEx(LPVOID pvReserved, DWORD dwCoInit);
```



El primer parámetro está reservado y debe ser **NULL.** El segundo parámetro especifica el modelo de subprocesos que usará el programa. COM admite dos modelos de subprocesos diferentes, *apartment threaded* *y multithreaded.* Si especifica subprocesos de apartamento, está realizando las siguientes garantías:

-   Tendrá acceso a cada objeto COM desde un único subproceso; no compartirá punteros de interfaz COM entre varios subprocesos.
-   El subproceso tendrá un bucle de mensajes. (Vea [Mensajes de ventana](window-messages.md) en el módulo 1).

Si alguna de estas restricciones no es verdadera, use el modelo multiproceso. Para especificar el modelo de subprocesos, establezca una de las marcas siguientes en el *parámetro dwCoInit.*



| Marca                          | Descripción         |
|-------------------------------|---------------------|
| **COINIT \_ APARTMENTTHREADED** | Apartamento subproceso. |
| **COINIT \_ MULTITHREADED**     | Multiproceso.      |



 

Debe establecer exactamente una de estas marcas. Por lo general, un subproceso que crea una ventana debe usar la marca **\_ COINIT APARTMENTTHREADED** y otros subprocesos deben usar **COINIT \_ MULTITHREADED**. Sin embargo, algunos componentes COM requieren un modelo de subprocesos determinado. En la documentación de MSDN se le debe decir cuándo es el caso.

> [!Note]  
> En realidad, incluso si especifica subprocesos de apartamento, todavía es posible compartir interfaces entre subprocesos mediante una técnica denominada *serialización*. La serialización está fuera del ámbito de este módulo. Lo importante es que, con el subprocesamiento de apartamento, nunca debe copiar simplemente un puntero de interfaz a otro subproceso. Para obtener más información sobre los modelos de subprocesos COM, vea [Procesos, subprocesos y departamentos](/windows/desktop/com/processes--threads--and-apartments).

 

Además de las marcas ya mencionadas, es una buena idea establecer la marca **COINIT \_ DISABLE \_ OLE1DDE** en el *parámetro dwCoInit.* Al establecer esta marca se evita cierta sobrecarga asociada a la vinculación e inserción de objetos (OLE) 1.0, una tecnología obsoleta.

A continuación se muestra cómo inicializaría COM para el subprocesamiento de apartamento:


```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE);
```



El tipo de valor devuelto **HRESULT** contiene un código de error o correcto. Veremos el control de errores COM en la sección siguiente.

## <a name="uninitializing-the-com-library"></a>Desinicializar la biblioteca COM

Para cada llamada correcta a [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex), debe llamar a [**CoUninitialize antes**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) de que se cierre el subproceso. Esta función no toma parámetros y no tiene ningún valor devuelto.


```C++
CoUninitialize();
```



## <a name="next"></a>Siguientes

[Códigos de error en COM](error-codes-in-com.md)

 

 