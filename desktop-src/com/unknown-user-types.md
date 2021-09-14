---
title: Tipos de usuario desconocidos
description: Tipos de usuario desconocidos
ms.assetid: c2a4bd83-6eaf-4130-8f86-e99f1e18b63d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4843ca2e19508806bba952403a2211a39f5a5ca
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160523"
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

 

 