---
description: Uso de la exclusión mutua para asf Secuencias
ms.assetid: fdd31eac-1dd6-45f0-90fb-d5a74c85db2e
title: Uso de la exclusión mutua para asf Secuencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40c7fd104659064952803c16f572ee1e55dee0508144474e89ee7c0f362315c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034573"
---
# <a name="using-mutual-exclusion-for-asf-streams"></a>Uso de la exclusión mutua para asf Secuencias

El contenido de ASF puede contener varias secuencias que se excluyen mutuamente. Estas secuencias no se pueden leer simultáneamente, pero solo se lee una de ellas a la vez. Por ejemplo, el archivo puede contener un conjunto de secuencias que incluyen el mismo contenido codificado a una velocidad de bits diferente. El flujo que se usa viene determinado por el ancho de banda disponible para la aplicación que transmite el contenido. El objeto de exclusión mutua de ASF, que forma parte del objeto de encabezado, almacena información sobre el grupo de secuencias mutuamente excluyentes.

En Media Foundation, el *objeto de exclusión* mutua que expone la interfaz [**RECORDSETASFMutualExclusion**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion) existe para cada objeto de exclusión mutua de ASF. El objeto de perfil contiene una referencia a todos los objetos de exclusión mutua.

El objeto de exclusión mutua almacena información sobre el grupo de flujos mutuamente excluyentes como registros. Un objeto de exclusión mutua puede tener varios registros que se pueden usar para crear escenarios complejos. Cada registro contiene una o varias secuencias que no pueden coexistir con secuencias de otro registro, mantenidas por el objeto de exclusión mutua, en función del tipo de exclusión mutua, como la velocidad de bits.

Un ejemplo común de exclusión mutua compleja es un archivo que contiene tres secuencias de audio del mismo contenido con varias velocidades de bits en cada uno de los tres idiomas. Solo se debe reproducir una de las nueve secuencias a la vez, pero hay dos tipos por los que son mutuamente excluyentes: idioma y velocidad de bits.

En este ejemplo, a las nueve secuencias se les asignan los siguientes números de secuencia:

<dl> 1 - Idioma 1, velocidad de bits 1  
2 - Idioma 1, velocidad de bits 2  
3 - Idioma 1, velocidad de bits 3  
4 - Idioma 2, velocidad de bits 1  
5 - Idioma 2, velocidad de bits 2  
6 - Idioma 2, velocidad de bits 3  
7 - Idioma 3, velocidad de bits 1  
8 - Idioma 3, velocidad de bits 2  
9 - Idioma 3, velocidad de bits 3  
</dl>

Este escenario se puede implementar mediante los cuatro objetos de exclusión mutua siguientes:

-   El primer objeto de exclusión mutua incluye flujos 1, 2 y 3, mutuamente excluyentes por velocidad de bits. Cada secuencia tiene su propio registro.
-   El segundo objeto de exclusión mutua incluye los flujos 4, 5 y 6, mutuamente excluyentes por velocidad de bits. Cada secuencia tiene su propio registro.
-   El tercer objeto de exclusión mutua incluye 7, 8 y 9, mutuamente excluyente por velocidad de bits. Cada secuencia tiene su propio registro.
-   El cuarto objeto de exclusión mutua contiene tres registros, el primero incluidos los flujos 1, 2 y 3; el segundo incluye las secuencias 4, 5 y 6; y el tercero, incluidos los flujos 7, 8 y 9. Estos registros se excluyen mutuamente por idioma.

Al reproducir un archivo creado de esta manera, la aplicación de streaming selecciona primero el idioma porque es menos probable que cambie en medio de la presentación y, a continuación, selecciona una velocidad de bits.

## <a name="mutual-exclusion-object-creation-and-configuration"></a>Creación y configuración de objetos de exclusión mutua

En la lista siguiente se resume el proceso de configuración de un objeto de exclusión mutua:

1.  Cree un objeto de exclusión mutua.
2.  Establezca el tipo de exclusión mutua.
3.  Configure el objeto de exclusión mutua agregando registros y los flujos asociados.
4.  Agregue el objeto de exclusión mutua al perfil.

Para crear y configurar un objeto de exclusión mutua

1.  Llame [**a IMFASFProfile::CreateMutualExclusion para**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createmutualexclusion) crear un objeto de exclusión mutua vacío.
2.  Llame [**a IMFASFMutualExclusion::SetType para**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-settype) establecer el criterio de la secuencia mutuamente excluyente.

    Las secuencias pueden ser mutuamente excluyentes por idioma, velocidad de bits, presentación y criterios personalizados. El tipo se representa como un GUID. Para obtener una lista de estas constantes, vea [ASF Mutual Exclusion Type GUIDs (GUID](asf-mutual-exclusion-type-guids.md)de tipo de exclusión mutua de ASF).

3.  Llame a [**IMFASFMutualExclusion::AddRecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-addrecord) para agregar un registro al objeto de exclusión mutua.

    Este método agrega un registro vacío y le asigna un índice de registro a partir de cero.

4.  Llame [**a IMFASFMutualExclusion::AddStreamForRecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-addstreamforrecord) para agregar el número de secuencia al registro especificado por el índice de registros.

    Cada registro incluye una o varias secuencias. Cada secuencia de un registro es mutuamente excluyente de todas las secuencias de todos los demás registros. Para obtener el número de secuencias de un registro, llame a [**IMFASFMutualExclusion::GetStreamsForRecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-getstreamsforrecord) especificando el índice del registro.

    Para quitar una secuencia del registro, llame a [**IMFASFMutualExclusion::RemoveStreamFromRecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-removestreamfromrecord) y especifique el índice de registro y el número de secuencia.

5.  Llame [**a IMFASFProfile::AddMutualExclusion para**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-addmutualexclusion) agregar el objeto de exclusión mutua configurado al perfil.

## <a name="enumerating-mutual-exclusion-objects-in-a-profile"></a>Enumerar objetos de exclusión mutua en un perfil

Si [**EL error DECIFProfile::AddMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-addmutualexclusion) se realiza correctamente, asigna un índice al objeto especificado, empezando por cero.

Para enumerar los objetos de exclusión mutua asociados a un perfil, llame a [**IMFASFProfile::GetMutualExclusionCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getmutualexclusioncount) y recorrer la lista mediante una llamada a [**IMFASFProfile::GetMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getmutualexclusion). Los índices de exclusión mutua son secuenciales y oscilan entre 0 y uno menos que el número de secuencias recuperadas por **GetMutualExclusionCount.**

Un objeto de exclusión mutua se quita del perfil mediante una llamada a [**IMFASFProfile::RemoveMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removemutualexclusion). El perfil reasigna los índices de exclusión mutua para que sean secuenciales a partir de cero. Esto sobrescribe los índices almacenados previamente, que ya no son válidos después de llamar a este método. Esto libera los registros de flujo de exclusión mutua asociados.

## <a name="removing-records-in-a-mutual-exclusion-object"></a>Quitar registros en un objeto de exclusión mutua

Para quitar un registro de un objeto de exclusión mutua, llame a [**IMFASFMutualExclusion::RemoveRecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-removerecord). Si este método se realiza correctamente, el objeto de exclusión mutua indexa los registros restantes para que sean secuenciales a partir de cero. La aplicación debe enumerar los registros para garantizar el índice correcto para cada registro. Para ello, llame a [**IMFASFMutualExclusion::GetRecordCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-getrecordcount) y realice un bucle por los registros mediante una llamada a [**ALFMutualExclusion::GetStreamsForRecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-getstreamsforrecord).

Quitar el registro con el índice más alto no tiene ningún efecto en los demás índices.

## <a name="modifying-a-mutual-exclusion-object"></a>Modificar un objeto de exclusión mutua

Para cambiar la configuración del objeto de exclusión mutua en el perfil, la aplicación debe reemplazar el objeto de exclusión mutua existente por otro objeto que contenga la nueva configuración.

Para cambiar la configuración del objeto de exclusión mutua en el perfil

1.  Enumerar los objetos de exclusión mutua en el perfil para obtener el objeto que debe cambiarse.
2.  Llame [**a IMFASFMutualExclusion::Clone**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-clone) para clonar el objeto de exclusión mutua.

3.  Configure el objeto clonado según sea necesario.
4.  Llame [**a IMFASFProfile::RemoveMutualExclusion para**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removemutualexclusion) quitar el antiguo objeto de exclusión mutua del perfil.

5.  Llame [**a IMFASFProfile::AddMutualExclusion para**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-addmutualexclusion) agregar el objeto de exclusión mutua actualizado al perfil.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Perfil de ASF](asf-profile.md)
</dt> </dl>

 

 



