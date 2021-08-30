---
title: Insertable (clave CLSID)
description: Indica que los objetos de esta clase deben aparecer en el cuadro de lista Cuadro de diálogo Insertar objeto cuando los usan las aplicaciones de contenedor COM.
ms.assetid: 908cbfc4-ebf8-454e-b2e5-34449de60e7f
keywords:
- COM de clave del Registro insertable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 699de5db82981e5f0f1db1229d31f96620adcb8c
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884320"
---
# <a name="insertable-clsid-key"></a>Insertable (clave CLSID)

Indica que los objetos de esta clase deben aparecer en el cuadro de lista Cuadro de **diálogo Insertar** objeto cuando los usan las aplicaciones de contenedor COM.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Insertable
```

## <a name="remarks"></a>Comentarios

Esta clave es una entrada necesaria para aplicaciones COM de 32 bits cuyos objetos se pueden insertar en aplicaciones de 16 bits existentes. Las aplicaciones de 16 bits existentes buscan en el Registro esta clave, lo que informa a la aplicación de que el servidor admite inserciones. Si existe **la clave Insertable,** las aplicaciones de 16 bits también pueden intentar comprobar que el servidor existe en la máquina. Las aplicaciones de 16 bits normalmente recuperan el valor de la clave [**LocalServer**](localserver.md) de la clase y comprueban si se trata de un archivo válido en el sistema. Por lo tanto, para que una aplicación de 32 bits pueda insertarse mediante una aplicación de 16 bits, la aplicación de 32 bits debe registrar la subclave **LocalServer** además de registrar [**LocalServer32**](localserver32.md).

Esta entrada, que se usa con controles, indica que un objeto solo puede actuar como un objeto incrustado en su lugar sin características de control especiales. Los objetos que tienen esta clave aparecen en el **cuadro de diálogo Insertar** objeto de su contenedor. Cuando se usa con controles, esta entrada también indica que el control se ha probado con contenedores que no son de control. Esta entrada también es opcional y se puede omitir cuando un control no está diseñado para trabajar con contenedores más antiguos que no entienden los controles.

> [!Note]  
> Esta clave no está presente para clases internas como las clases de moniker.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**&lt;ProgID&gt;**](-progid--key.md)
</dt> </dl>

 

 




