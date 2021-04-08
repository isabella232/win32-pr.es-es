---
title: Clave ProgID
description: Un identificador de programación (ProgID) es una entrada del registro que se puede asociar a un CLSID. Al igual que el CLSID, el ProgID identifica una clase pero con menos precisión porque no se garantiza que sea globalmente único.
ms.assetid: f9ef2934-0815-4a6f-9283-8f748eee083b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a9ef64515d2dda4512af0086970cb2ab61b4830
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104078738"
---
# <a name="progid-key"></a>Clave ProgID

Un identificador de programación (ProgID) es una entrada del registro que se puede asociar a un CLSID. Al igual que el CLSID, el ProgID identifica una clase pero con menos precisión porque no se garantiza que sea globalmente único.

## <a name="registry-entry"></a>Entrada del Registro

**HKEY \_ \_Clases de \\ software \\ de máquina local** \\ *{* ProgID *}*



| Clave del Registro                            | Descripción                                                        |
|-----------------------------------------|--------------------------------------------------------------------|
| [**CLSID**](clsid.md)                  | Asocia un ProgID a un CLSID.                                  |
| [**Insertable**](insertable-progid.md) | Indica que esta clase se va a insertar en contenedores OLE 2.       |
| [**Protocolo**](protocol.md)            | Indica que esta clase OLE 2 se va a insertar en contenedores OLE 1. |
| [**Shell**](shell.md)                  | Proporciona la impresión del shell de Windows 3,1 y la información **abierta del archivo** . |



 

## <a name="remarks"></a>Observaciones

Puede usar un ProgID en situaciones de programación en las que no sea posible usar un CLSID. Los ProgID no deben aparecer en la interfaz de usuario. No se garantiza que los ProgID sean únicos, por lo que solo se pueden usar si los conflictos de nombres son administrables.

El formato de un ProgID es <*programa*> *. <>* de la *versión* <, separados por puntos y sin espacios, como en> ument. 6. El ProgID debe cumplir los siguientes requisitos:

-   No debe tener más de 39 caracteres.
-   No contenga signos de puntuación (incluidos los guiones bajos) excepto uno o más puntos.
-   No empieza por un dígito.
-   Ser diferente del nombre de clase de cualquier aplicación OLE 1, incluida la versión OLE 1 de la misma aplicación, si hay alguna.

Dado que el ProgID no debe aparecer en la interfaz de usuario, puede obtener un nombre que se pueda mostrar llamando a [**IOleObject:: GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype). Consulte también [**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype).

La clave **HKEY \_ local \_ Machine \\ software \\ classes** corresponde a la clave **\_ \_ raíz de las clases HKEY** , que se conserva por compatibilidad con versiones anteriores de com.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IOleObject:: GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype)
</dt> <dt>

[**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype)
</dt> </dl>

 

 




