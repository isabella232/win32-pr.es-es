---
description: Revocación de certificados de OPM
ms.assetid: 21faf809-1335-4d93-be06-628c5a05a4c8
title: Revocación de certificados de OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47ebf38a3fa6bd2b61a756d6103453fd0356f693
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092733"
---
# <a name="opm-certificate-revocation"></a>Revocación de certificados de OPM

Microsoft puede revocar un certificado de administrador de protección de salida (OPM). La lista de certificados revocados se almacena en una lista de revocación global (GRL). La GRL tiene el formato siguiente:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Sección</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Encabezado</td>
<td>Estructura <a href="grl-header.md"><strong>GRL_HEADER</strong></a> datos.</td>
</tr>
<tr class="even">
<td>Core</td>
<td>Contiene las siguientes listas de revocación:
<ul>
<li>Revocaciones binarias de kernel</li>
<li>Revocaciones binarias en modo de usuario</li>
<li>Revocaciones de certificados</li>
<li>Raíces de confianza (reservadas)</li>
</ul>
La lista de raíces de confianza no se usa actualmente y está reservada para su uso futuro.</td>
</tr>
<tr class="odd">
<td>Entradas extensibles</td>
<td>Contiene información utilizada por otros componentes. Esta sección no es relevante para OPM.</td>
</tr>
<tr class="even">
<td>Renovaciones:</td>
<td>Contiene GUID que definen Windows Update identificadores. Esta sección contiene identificadores para las listas siguientes:
<ul>
<li>Revocaciones binarias de kernel</li>
<li>Revocaciones binarias en modo de usuario</li>
<li>Revocaciones de certificados</li>
</ul>
Una aplicación puede usar estos identificadores para solicitar una versión renovado de un binario revocado, si hay alguno disponible.</td>
</tr>
<tr class="odd">
<td>Firma: sección Principal</td>
<td>Firma las secciones de encabezado y núcleo.</td>
</tr>
<tr class="even">
<td>Firma: sección Extensible</td>
<td>Firma el encabezado y las secciones extensibles.</td>
</tr>
</tbody>
</table>



 

El encabezado GRL es una [**estructura GRL \_ HEADER.**](grl-header.md) El **miembro dwSequenceNumber** de la estructura contiene el número de versión grl. Este número se incrementa cada vez que se actualiza la GRL y se coloca una nueva versión en el equipo del usuario.

Los certificados OPM revocados se enumeran en la lista de revocaciones de certificados de la sección Core. Cada entrada Core de grl es una matriz de 20 bytes que contiene el hash SHA-1 de la clave pública del certificado revocado.

Las secciones Firma contienen firmas que se pueden usar para comprobar que la GRL no se ha alterado. Cada sección signature contiene una estructura [**MF \_ SIGNATURE.**](mf-signature.md) La primera firma firma el encabezado más la sección Core. La segunda firma firma el encabezado más la sección Extensible; esta firma no es relevante para OPM.

Para asegurarse de que la GRL no se ha alterado, compruebe la firma como se muestra a continuación:

1.  Busque el inicio de la [**estructura MF \_ SIGNATURE.**](mf-signature.md) La ubicación de la **estructura MF \_ SIGNATURE** se da en el **miembro cbSignatureCoreOffset** de la [**estructura GRL \_ HEADER.**](grl-header.md) La ubicación se especifica como un desplazamiento en bytes desde el inicio de grl.
2.  Analice la estructura [**MF \_ SIGNATURE**](mf-signature.md) como una firma PKCS \# 7 con una cadena de certificados.
3.  Compruebe la cadena de certificados hasta una raíz de confianza.
4.  Compruebe que el certificado hoja tiene el siguiente identificador de objeto en el EKU: "1.3.6.1.4.1.311.10.5.4".
5.  Calcule un hash de los bytes que incluyen el encabezado y las secciones principales de grl.
6.  Compruebe que el hash coincide con la firma del certificado hoja.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administrador de protección de salida](output-protection-manager.md)
</dt> <dt>

[**ENCABEZADO \_ GRL**](grl-header.md)
</dt> <dt>

[**MF \_ SIGNATURE**](mf-signature.md)
</dt> </dl>

 

 



