---
description: Los proveedores pueden llamar a métodos implementados por WMI desde sus implementaciones de método.
ms.assetid: 5bfd9d9b-ffe5-4def-a97d-85c4c01223f0
ms.tgt_platform: multiple
title: Realizar llamadas a WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 534e478336cdd9675e382ef9b089f2d7bc595b03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082695"
---
# <a name="making-calls-to-wmi"></a>Realizar llamadas a WMI

Los proveedores pueden llamar a métodos implementados por WMI desde sus implementaciones de método. Sin embargo, existen consideraciones especiales cuando un proveedor llama a la implementación WMI de un método [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) desde su propia implementación del mismo método. Estas consideraciones son importantes independientemente de si el proveedor llama a la versión sincrónica o asincrónica del método.

Cada método [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) que un proveedor puede implementar tiene un parámetro *pCtx* , un puntero a una implementación de la interfaz [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) . Cuando WMI llama al proveedor, WMI pasa un puntero válido en este parámetro. Un proveedor siempre debe pasar este mismo puntero en cualquier llamada a WMI que realicen mientras se atienden las solicitudes. Descuidarse de establecer *pCtx* correctamente puede hacer que WMI inicie un bucle infinito.

En el ejemplo de código siguiente se muestra la manera correcta de llamar a la implementación WMI de [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) desde dentro de una implementación de [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).


```C++
STDMETHODIMP CClassProv::GetObjectAsync (BSTR ObjectPath,
    long lFlags, IWbemContext *pCtx,
    IWbemObjectSink *pHandler)
{
  IWbemClassObject *pclObj = NULL;
  IWbemServices* m_pNamespace;
  HRESULT hr = m_pNamespace->GetObject(
      _bstr_t(L"AClass"), 0, pCtx, &pclObj, 
      NULL );
  pclObj->Release();
  return pHandler->SetStatus(0, hr, NULL, NULL);
}
```



El ejemplo de código de C++ de este tema requiere las siguientes referencias e \# incluir instrucciones para compilar correctamente.


```C++
#define _WIN32_DCOM
#include <iostream>
using namespace std;
#include <comdef.h>
#include <Wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```



Los proveedores de instancia, clase y propiedad no deben emitir llamadas a WMI que soliciten la modificación de los datos mientras atienden una solicitud de lectura. Los únicos proveedores que son excepciones a esta regla son los proveedores de inserciones. Un proveedor de inserciones es un proveedor de clases que almacena los datos en el repositorio WMI y se basa en WMI para controlar las solicitudes de los clientes. Mientras se atiende una solicitud de lectura, un proveedor de inserciones puede actualizar el repositorio WMI, pero debe establecer el parámetro *lFlags* en la marca WBEM de la llamada a **\_ \_ Owner \_** en la llamada a [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) adecuada.

Los proveedores de eventos no deben realizar ningún cambio de clase mientras atienden una llamada. Tampoco pueden emitir llamadas relacionadas con eventos, como modificar un filtro de eventos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desarrollar un proveedor WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Configuración de descriptores de seguridad de espacio](setting-namespace-security-descriptors.md)
</dt> <dt>

[Protección del proveedor](securing-your-provider.md)
</dt> </dl>

 

 



