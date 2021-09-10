---
title: ProgID Key
description: Un identificador de programación (ProgID) es una entrada del Registro que se puede asociar a un CLSID. Al igual que el CLSID, progID identifica una clase pero con menos precisión porque no se garantiza que sea única globalmente.
ms.assetid: f9ef2934-0815-4a6f-9283-8f748eee083b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a9ef64515d2dda4512af0086970cb2ab61b4830
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369491"
---
# <a name="progid-key"></a>ProgID Key

Un identificador de programación (ProgID) es una entrada del Registro que se puede asociar a un CLSID. Al igual que el CLSID, progID identifica una clase pero con menos precisión porque no se garantiza que sea única globalmente.

## <a name="registry-entry"></a>Entrada del Registro

**HKEY \_ Clases \_ DE SOFTWARE DE MÁQUINA \\ \\ LOCAL** \\ *{* ProgID *}*



| Clave del Registro                            | Descripción                                                        |
|-----------------------------------------|--------------------------------------------------------------------|
| [**CLSID**](clsid.md)                  | Asocia un ProgID a un CLSID.                                  |
| [**Insertable**](insertable-progid.md) | Indica que esta clase se puede insertar en contenedores OLE 2.       |
| [**Protocolo**](protocol.md)            | Indica que esta clase OLE 2 se puede insertar en contenedores OLE 1. |
| [**Shell**](shell.md)                  | Proporciona Windows de shell 3.1 e **información de apertura de** archivos. |



 

## <a name="remarks"></a>Observaciones

Puede usar un ProgID en situaciones de programación en las que no es posible usar un CLSID. Los progID no deben aparecer en la interfaz de usuario. No se garantiza que los progID sean únicos, por lo que solo se pueden usar cuando se pueden administrar conflictos de nombres.

El formato de un ProgID  es <Program>.<*Component*>.<*Version*>, separado por puntos y sin espacios, como en Word.Document.6. ProgID debe cumplir los siguientes requisitos:

-   No tiene más de 39 caracteres.
-   No contenga signos de puntuación (incluidos los caracteres de subrayado), excepto uno o varios puntos.
-   No empiece con un dígito.
-   Sea diferente del nombre de clase de cualquier aplicación OLE 1, incluida la versión OLE 1 de la misma aplicación, si hay una.

Dado que el ProgID no debe aparecer en la interfaz de usuario, puede obtener un nombre que se pueda mostrar llamando a [**IOleObject::GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype). Vea también [**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype).

La **clave HKEY \_ LOCAL MACHINE \_ SOFTWARE \\ \\ Classes** corresponde a la clave RAÍZ **HKEY \_ CLASSES, \_** que se conservaba por compatibilidad con versiones anteriores de COM.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IOleObject::GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype)
</dt> <dt>

[**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype)
</dt> </dl>

 

 




