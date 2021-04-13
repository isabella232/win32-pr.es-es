---
description: .
ms.assetid: 21faf809-1335-4d93-be06-628c5a05a4c8
title: Revocación de certificados OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e4b20dc00b0bd23644ef9dca22558a304ca9438
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543878"
---
# <a name="opm-certificate-revocation"></a>Revocación de certificados OPM

Microsoft puede revocar un certificado de administrador de protección de salida (OPM). La lista de certificados revocados se almacena en una lista de revocación global (GRL). El GRL tiene el siguiente formato:



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
<td>Estructura de <a href="grl-header.md"><strong>GRL_HEADER</strong></a> .</td>
</tr>
<tr class="even">
<td>Core</td>
<td>Contiene las siguientes listas de revocación:
<ul>
<li>Revocación binarias del kernel</li>
<li>Revocaciones binarias de modo de usuario</li>
<li>Revocación de certificados</li>
<li>Raíces de confianza (reservadas)</li>
</ul>
La lista de raíces de confianza no se utiliza actualmente y está reservada para un uso futuro.</td>
</tr>
<tr class="odd">
<td>Entradas extensibles</td>
<td>Contiene información que usan otros componentes. Esta sección no es relevante para OPM.</td>
</tr>
<tr class="even">
<td>Renovaciones</td>
<td>Contiene los GUID que definen Windows Update identificadores. Esta sección contiene los identificadores de las listas siguientes:
<ul>
<li>Revocación binarias del kernel</li>
<li>Revocaciones binarias de modo de usuario</li>
<li>Revocación de certificados</li>
</ul>
Una aplicación puede utilizar estos identificadores para solicitar una versión renovada de un binario revocado, si hay alguno disponible.</td>
</tr>
<tr class="odd">
<td>Firma: sección principal</td>
<td>Firma las secciones de encabezado y principal.</td>
</tr>
<tr class="even">
<td>Firma: sección extensible</td>
<td>Firma el encabezado y las secciones extensibles.</td>
</tr>
</tbody>
</table>



 

El encabezado GRL es una estructura de [**\_ encabezado GRL**](grl-header.md) . El miembro **dwSequenceNumber** de la estructura contiene el número de versión de GRL. Este número se incrementa cada vez que se actualiza el GRL y se coloca una nueva versión en el equipo del usuario.

Los certificados OPM revocados se enumeran en la lista de revocación de certificados de la sección principal. Cada entrada principal del GRL es una matriz de 20 bytes que contiene el hash de SHA-1 de la clave pública del certificado revocado.

Las secciones Signature contiene firmas que se pueden usar para comprobar que el GRL no se ha alterado. Cada una de las secciones Signature contiene la estructura de [**\_ firma AM MF**](mf-signature.md) . La primera firma firma el encabezado más la sección principal. La segunda firma firma el encabezado más la sección extensible; Esta firma no es relevante para OPM.

Para asegurarse de que el GRL no se ha manipulado, Compruebe la firma de la siguiente manera:

1.  Busque el inicio de la estructura de [**\_ firma MF**](mf-signature.md) . La ubicación de la estructura de **\_ firma MF** se proporciona en el miembro **cbSignatureCoreOffset** de la estructura de [**\_ encabezado GRL**](grl-header.md) . La ubicación se especifica como un desplazamiento en bytes desde el inicio del GRL.
2.  Analice la estructura de [**\_ firma MF**](mf-signature.md) como una \# firma PKCS 7 con una cadena de certificados.
3.  Compruebe la cadena de certificados hasta una raíz de confianza.
4.  Compruebe que el certificado de hoja tiene el siguiente identificador de objeto en el EKU: "1.3.6.1.4.1.311.10.5.4".
5.  Calcule un hash de los bytes que incluyen el encabezado y las secciones principales del GRL.
6.  Compruebe que el hash coincide con la firma del certificado de hoja.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administrador de protección de salida](output-protection-manager.md)
</dt> <dt>

[**\_encabezado GRL**](grl-header.md)
</dt> <dt>

[**\_firma MF**](mf-signature.md)
</dt> </dl>

 

 



