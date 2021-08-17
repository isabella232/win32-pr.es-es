---
title: Tipos de usuario desconocidos
description: Tipos de usuario desconocidos
ms.assetid: c2a4bd83-6eaf-4130-8f86-e99f1e18b63d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72ce5ee88d36399187bab24ce51f0ef1c3c074182f98ce30ff6dc7d370992ffd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129467"
---
# <a name="unknown-user-types"></a>Tipos de usuario desconocidos

Puede facilitar la localización del producto agregando la siguiente clave del Registro:

**HKEY \_ LOCAL \_ MACHINES SOFTWARE Microsoft \\ \\ \\ OLE2** \\ **UnknownUserType**  =  *usertype*

Esta clave permite a las funciones devolver una cadena especificada en lugar de un valor predeterminado de "Unknown", lo que permite a los localizadores especificar un tipo de usuario de un idioma diferente.

La implementación del controlador predeterminado COM de [**IOleObject::GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype) examina el Registro mediante una llamada [**a OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype). Si la clase del objeto no se encuentra en el Registro, se devuelve el tipo de usuario de la instancia [**de IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) del objeto. Si la clase no se encuentra en la instancia **de IStorage** del objeto, se devuelve la cadena "Unknown".

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registro de aplicaciones COM](registering-com-applications.md)
</dt> </dl>

 

 