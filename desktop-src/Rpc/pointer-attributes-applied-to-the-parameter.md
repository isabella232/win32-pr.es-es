---
title: Atributos de puntero aplicados al parámetro
description: Cada atributo de puntero (\ Ref \, \ Unique \ y \ PTR \) tiene características que afectan a la asignación de memoria. En la tabla siguiente se resumen estas características.
ms.assetid: 25a609cd-efe7-4cbb-b80e-b6a3ad8cda38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c7710fb3c39702b2b2fdb789ed1218dc88d44ea
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078199"
---
# <a name="pointer-attributes-applied-to-the-parameter"></a>Atributos de puntero aplicados al parámetro

Cada atributo de puntero ( \[ [ref](/windows/desktop/Midl/ref) \] , \[ [Unique](/windows/desktop/Midl/unique) \] y \[ [ptr](/windows/desktop/Midl/ptr) \] ) tiene características que afectan a la asignación de memoria. En la tabla siguiente se resumen estas características.



| Atributo de puntero       | Cliente                                                                                                                                                                                                            | Servidor                                                              |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| Referencia ( \[ **ref** \] ) | La aplicación cliente debe asignar.                                                                                                                                                                                 | Control especial necesario para punteros de nivel de nontop de solo **\[ salida \]**. |
| Único ( \[ **único** \] ) | Si es un parámetro, la aplicación cliente debe asignar; Si está incrustado, puede ser null. Cambiar de null a no NULL hace que el código auxiliar de cliente se asigne; Si se cambia de un valor distinto de null a NULL, se puede producir un huérfano.<br/> |                                                                     |
| Completo ( \[ **ptr** \] )      | Si es un parámetro, la aplicación cliente debe asignar; Si está incrustado, puede ser null. Cambiar de null a no NULL hace que el código auxiliar de cliente se asigne; Si se cambia de un valor distinto de null a NULL, se puede producir un huérfano.<br/> |                                                                     |



 

El atributo **\[ ref \]** indica que el puntero apunta a la memoria válida. Por definición, la aplicación cliente debe asignar toda la memoria que requieran los punteros de referencia.

El puntero único puede cambiar de null a un valor distinto de NULL. Si el puntero único cambia de null a no NULL, se asignará una nueva memoria en el cliente. Si el puntero único cambia de distinto de null a NULL, se puede producir el huérfano. Para obtener más información, consulte [memoria huérfana](memory-orphaning.md).

 

