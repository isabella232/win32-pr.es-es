---
title: Atributos de puntero aplicados al parámetro
description: Cada atributo de puntero (\ ref\ , \ unique\ y \ ptr\ ) tiene características que afectan a la asignación de memoria. En la tabla siguiente se resumen estas características.
ms.assetid: 25a609cd-efe7-4cbb-b80e-b6a3ad8cda38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c7710fb3c39702b2b2fdb789ed1218dc88d44ea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161037"
---
# <a name="pointer-attributes-applied-to-the-parameter"></a>Atributos de puntero aplicados al parámetro

Cada atributo de puntero ( \[ [ref](/windows/desktop/Midl/ref) \] , \[ [unique](/windows/desktop/Midl/unique) \] y \[ [ptr](/windows/desktop/Midl/ptr)) tiene características que afectan a la \] asignación de memoria. En la tabla siguiente se resumen estas características.



| Atributo pointer       | Cliente                                                                                                                                                                                                            | Servidor                                                              |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| Referencia ( \[ **ref** \] ) | La aplicación cliente debe asignarse.                                                                                                                                                                                 | Se necesita un control especial **\[ para \]** los punteros que no son de nivel superior. |
| Único \[ **(único)** \] | Si es un parámetro, la aplicación cliente debe asignar; si se incrusta, puede ser NULL. El cambio de null a non-null hace que se asigne el código auxiliar del cliente; Cambiar de un valor distinto de NULL a null puede provocar huérfanos.<br/> |                                                                     |
| Full ( \[ **ptr** \] )      | Si es un parámetro, la aplicación cliente debe asignar; si se incrusta, puede ser NULL. El cambio de null a non-null hace que se asigne el código auxiliar del cliente; Cambiar de un valor distinto de NULL a null puede provocar huérfanos.<br/> |                                                                     |



 

El **\[ atributo ref \]** indica que el puntero apunta a la memoria válida. Por definición, la aplicación cliente debe asignar toda la memoria que requieren los punteros de referencia.

El puntero único puede cambiar de NULL a non-null. Si el puntero único cambia de null a non-null, se asigna nueva memoria en el cliente. Si el puntero único cambia de distinto de NULL a null, puede producirse la huérfana. Para obtener más información, vea [Memoria huérfana.](memory-orphaning.md)

 

