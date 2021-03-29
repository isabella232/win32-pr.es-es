---
title: Tipos de usuarios desconocidos
description: Tipos de usuarios desconocidos
ms.assetid: c2a4bd83-6eaf-4130-8f86-e99f1e18b63d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4843ca2e19508806bba952403a2211a39f5a5ca
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104359454"
---
# <a name="unknown-user-types"></a>Tipos de usuarios desconocidos

Puede facilitar la localización del producto agregando la siguiente clave del registro:

**HKEY \_ \_Software de equipos locales \\ \\ Microsoft \\ OLE2** \\ **UnknownUserType**  =  *usertype*

Esta clave permite que las funciones devuelvan una cadena especificada en lugar de un valor predeterminado de "Unknown", lo que permite a los localizadores especificar un tipo de usuario de otro idioma.

La implementación del controlador predeterminado de COM de [**IOleObject:: GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype) examina el registro llamando a [**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype). Si la clase del objeto no se encuentra en el registro, se devuelve el tipo de usuario de la instancia de [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) del objeto. Si no se encuentra la clase en la instancia **IStorage** del objeto, se devuelve la cadena "Unknown".

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registro de aplicaciones COM](registering-com-applications.md)
</dt> </dl>

 

 