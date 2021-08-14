---
title: Atributos de puntero aplicados al parámetro
description: Cada atributo de puntero (\ ref\ , \ unique\ y \ ptr\ ) tiene características que afectan a la asignación de memoria. En la tabla siguiente se resumen estas características.
ms.assetid: 25a609cd-efe7-4cbb-b80e-b6a3ad8cda38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bcc6649dc663d7b029a7d7f345719330719d2eb19b6b7a63fa02797c17df16c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927500"
---
# <a name="pointer-attributes-applied-to-the-parameter"></a>Atributos de puntero aplicados al parámetro

Cada atributo de puntero \[ [(ref,](/windows/desktop/Midl/ref) \] \[ [unique](/windows/desktop/Midl/unique) \] y \[ [ptr)](/windows/desktop/Midl/ptr)tiene características que afectan a la \] asignación de memoria. En la tabla siguiente se resumen estas características.



| Atributo de puntero       | Cliente                                                                                                                                                                                                            | Servidor                                                              |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| Referencia ( \[ **ref** \] ) | La aplicación cliente debe asignarse.                                                                                                                                                                                 | Se necesita un control especial **\[ para \]** los punteros que no son de nivel superior. |
| Único \[ **(único)** \] | Si un parámetro, la aplicación cliente debe asignar; si está incrustado, puede ser NULL. El cambio de null a non-null hace que se asigne el código auxiliar del cliente; Cambiar de un valor distinto de NULL a null puede provocar un huérfano.<br/> |                                                                     |
| Full ( \[ **ptr** \] )      | Si un parámetro, la aplicación cliente debe asignar; si está incrustado, puede ser NULL. El cambio de null a non-null hace que se asigne el código auxiliar del cliente; Cambiar de un valor distinto de NULL a null puede provocar un huérfano.<br/> |                                                                     |



 

El **\[ atributo ref \]** indica que el puntero apunta a la memoria válida. Por definición, la aplicación cliente debe asignar toda la memoria que requieren los punteros de referencia.

El puntero único puede cambiar de null a non-null. Si el puntero único cambia de NULL a no NULL, se asigna nueva memoria en el cliente. Si el puntero único cambia de distinto de NULL a NULL, puede producirse la huérfana. Para obtener más información, vea [Memoria huérfana.](memory-orphaning.md)

 

