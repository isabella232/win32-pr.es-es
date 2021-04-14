---
title: Códigos de error de dispositivo
description: Los métodos InvokeAction y QueryStateVariable devuelven valores HRESULT que podrían indicar un error de dispositivo (es decir, un error que se recibe de un dispositivo certificado con UPnP).
ms.assetid: 4b18a5d4-f6e8-4670-93dd-ecd012940000
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfcd92d79897318ae6e45fac918dce6af2fe647b
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "104488434"
---
# <a name="device-error-codes"></a>Códigos de error de dispositivo

Los métodos [**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) y [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) devuelven valores **HRESULT** que podrían indicar un error de dispositivo (es decir, un error que se recibe de un dispositivo certificado con UPnP). Si se recibe un error de un dispositivo, el método ([**InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) o [**QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable)) devuelve un valor **HRESULT** que se basa en el código de error del dispositivo, tal como se explica en este tema. Dado que se aplica una conversión al código de error del dispositivo para generar un valor **HRESULT** , no se puede leer el código de error del dispositivo directamente desde el valor **HRESULT** .

## <a name="conversion-of-a-device-error-code-to-an-hresult"></a>Conversión de un código de error de dispositivo a un valor HRESULT

Hay códigos de error de dispositivo estándar y no estándar. Los códigos estándar tienen el mismo significado en todos los dispositivos certificados para UPnP y tienen valores inferiores a 600. Los códigos no estándar son específicos del proveedor y tienen valores comprendidos entre 600 y 899.

Tanto si el código de error del dispositivo es estándar como si no, determina cómo se genera el valor **HRESULT** :

-   Un código de error de dispositivo estándar se asigna a un valor **HRESULT** .

<!-- -->

-   Un código de error de dispositivo no estándar se incrusta en el valor **HRESULT** aplicando una fórmula.

Ambos procedimientos se pueden invertir para determinar el código de error de dispositivo a partir de un valor **HRESULT** determinado.

## <a name="deriving-a-device-error-code-from-an-hresult-value"></a>Derivar un código de error de dispositivo de un valor HRESULT

Si el valor **HRESULT** es mayor o igual que la **\_ \_ \_ \_ base específica de la acción de UPnP e** (0x80040300) y es menor o igual que el **\_ \_ \_ \_ número máximo específico de acciones de UPnP e** (0x8004042B), el código de error del dispositivo no es estándar. Use la fórmula de la sección siguiente para determinar el código de error. De lo contrario, el código de error del dispositivo es estándar. Use la tabla de la sección asignación de códigos de error de dispositivo estándar, que proporciona la asignación del valor **HRESULT** al código de error del dispositivo.

Para obtener una descripción de texto del error después de una llamada a [**IUPnPService:: InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction), establezca el parámetro *pvarRetVal* en una matriz vacía. En el momento de la devolución, este parámetro contendrá una descripción de texto del error, si se produjo alguno.

### <a name="formula-for-nonstandard-device-error-codes"></a>Fórmula para códigos de error de dispositivo no estándar

Use la siguiente fórmula si **la \_ \_ \_ \_ base específica de la acción UPnP e** no es el **valor** **\_ \_ \_ \_ máximo específico de la acción de UPnP e**.

Código de error de dispositivo **= (**  -  **\_ \_ \_ \_ base específica de la acción de UPnP E** **\_ \_ \_**

Sustituir los valores numéricos reales, la ecuación es: código de error de dispositivo = (**HRESULT** -0x80040300) + 0x0258

### <a name="mapping-for-standard-device-error-codes"></a>Asignación de códigos de error de dispositivo estándar

Use la siguiente **asignación si la**  <  **\_ \_ \_ \_ base específica de la acción de UPnP E** de la acción.



| Valor HRESULT                    | Código de error de dispositivo                | Valor real |
|----------------------------------|----------------------------------|--------------|
| \_ \_ acción no válida de UPnP E \_         | \_acción no válida de error \_           | 401          |
| \_ \_ argumentos no válidos de UPnP E \_      | argumento de error \_ no válido \_              | 402          |
| UPNP \_ E \_ no \_ \_ sincronizados           | ERROR \_ de \_ número de secuencia no válido \_ | 403          |
| \_ \_ variable no válida de UPnP E \_       | ERROR \_ de \_ variable no válida         | 404          |
| \_error de \_ solicitud de acción \_ \_ de UPnP E | \_ \_ error interno del dispositivo de error \_   | 501          |



 

## <a name="more-information"></a>Más información

Los códigos de error de dispositivo se especifican en la [versión 1,0 de la arquitectura del dispositivo UPnP](https://openconnectivity.org/resources/documents.asp). Las constantes mencionadas en este tema se definen en los archivos UPnP. h y UPnP. idl.

 

 




