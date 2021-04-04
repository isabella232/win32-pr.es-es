---
title: Insertable (clave CLSID)
description: Indica que los objetos de esta clase deben aparecer en el cuadro de lista del cuadro de diálogo Insertar objeto cuando lo usan las aplicaciones de contenedor COM.
ms.assetid: 908cbfc4-ebf8-454e-b2e5-34449de60e7f
keywords:
- COM de clave del registro insertable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5da4892fb13de5954dabe7c55759900dba32f854
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104078758"
---
# <a name="insertable-clsid-key"></a>Insertable (clave CLSID)

Indica que los objetos de esta clase deben aparecer en el cuadro de lista del cuadro de diálogo **Insertar objeto** cuando lo usan las aplicaciones de contenedor com.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Insertable
```

## <a name="remarks"></a>Observaciones

Esta clave es una entrada necesaria para las aplicaciones COM de 32 bits cuyos objetos se pueden insertar en las aplicaciones de 16 bits existentes. Las aplicaciones de 16 bits existentes buscan esta clave en el registro, lo que informa a la aplicación de que el servidor admite la incrustación. Si la clave **insertable** existe, las aplicaciones de 16 bits también pueden intentar comprobar que el servidor existe en el equipo. las aplicaciones de 16 bits normalmente recuperan el valor de la clave [**LocalServer**](localserver.md) de la clase y comprueban si es un archivo válido en el sistema. Por lo tanto, para que una aplicación de 16 bits pueda insertar una aplicación de 32 bits, la aplicación de 32 bits debe registrar la subclave **LocalServer** además de registrar [**LocalServer32**](localserver32.md).

Cuando se usa con controles, esta entrada indica que un objeto solo puede actuar como un objeto incrustado en contexto sin características de control especiales. Los objetos que tienen esta clave aparecen en el cuadro de diálogo **Insertar objeto** para su contenedor. Cuando se usa con controles, esta entrada también indica que el control se ha probado con contenedores que no son de control. Esta entrada también es opcional y se puede omitir cuando un control no está diseñado para trabajar con contenedores más antiguos que no entienden los controles.

> [!Note]  
> Esta clave no está presente para las clases internas como las clases moniker.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**<ProgID>**](-progid--key.md)
</dt> </dl>

 

 




