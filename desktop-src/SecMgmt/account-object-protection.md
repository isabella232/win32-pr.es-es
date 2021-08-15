---
description: Explica cómo se protegen los objetos Account.
ms.assetid: a07ef46e-f4b6-4e21-bdd7-72d03e1c88b3
title: Protección de objetos de cuenta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c49610827c8f27b2ad1dd645faca1374534b9d4acb8353421fc55901da724dd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117969764"
---
# <a name="account-object-protection"></a>Protección de objetos de cuenta

[**Los objetos**](account-object.md) de cuenta están protegidos de la manera siguiente:

-   El grupo **WORLD** tiene GENERIC \_ EXECUTE.
-   El administrador **local \_ del grupo** tiene acceso DELETE, GENERIC \_ READ, GENERIC \_ WRITE, GENERIC EXECUTE y WRITE \_ \_ DACL.
-   El administrador **local \_ del grupo** se asigna como propietario y grupo principal de objetos de cuenta.

 

 



