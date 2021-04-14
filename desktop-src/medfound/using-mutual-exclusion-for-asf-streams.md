---
description: Usar exclusión mutua para secuencias ASF
ms.assetid: fdd31eac-1dd6-45f0-90fb-d5a74c85db2e
title: Usar exclusión mutua para secuencias ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 411b5aa0638ab1c56298b93d01e8de99920abc6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648291"
---
# <a name="using-mutual-exclusion-for-asf-streams"></a>Usar exclusión mutua para secuencias ASF

El contenido ASF puede contener varias secuencias que son mutuamente excluyentes. Estas secuencias no se pueden leer simultáneamente, pero solo una de ellas se lee a la vez. Por ejemplo, el archivo puede contener un conjunto de secuencias que incluye el mismo contenido codificado a una velocidad de bits diferente. La secuencia que se utiliza está determinada por el ancho de banda disponible para la aplicación que transmite el contenido. El objeto de exclusión mutua de ASF, que forma parte del objeto de encabezado, almacena información sobre el grupo de flujos mutuamente excluyentes.

En Media Foundation, existe el objeto de *exclusión mutua* que expone la interfaz [**IMFASFMutualExclusion**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion) para cada objeto de exclusión mutua de ASF. El objeto de perfil contiene referencias a todos los objetos de exclusión mutua.

El objeto de exclusión mutua almacena información sobre el grupo de flujos mutuamente excluyentes como registros. Un objeto de exclusión mutua puede tener varios registros que se pueden usar para crear escenarios complejos. Cada registro contiene una o más secuencias que no pueden coexistir con secuencias en otro registro, mantenidas por el objeto de exclusión mutua, en función del tipo de exclusión mutua, como la velocidad de bits.

Un ejemplo común de exclusión mutua compleja es un archivo que contiene tres flujos de audio del mismo contenido con varias velocidades de bits en cada uno de tres idiomas. Solo se debe reproducir una de las nueve secuencias a la vez, pero hay dos tipos por los que se excluyen mutuamente: el lenguaje y la velocidad de bits.

En este ejemplo, a las nueve secuencias se les asignan los números de secuencia siguientes:

<dl> 1-idioma 1, velocidad de bits 1  
2-idioma 1, velocidad de bits 2  
3-idioma 1, tasa de bits 3  
4-idioma 2, velocidad de bits 1  
5-idioma 2, velocidad de bits 2  
6-idioma 2, tasa de bits 3  
7-idioma 3, velocidad de bits 1  
8-idioma 3, velocidad de bits 2  
9-idioma 3, tasa de bits 3  
</dl>

Este escenario se puede implementar mediante el uso de los cuatro objetos de exclusión mutua siguientes:

-   El primer objeto de exclusión mutua incluye las secuencias 1, 2 y 3, mutuamente excluyentes según la velocidad de bits. Cada flujo tiene su propio registro.
-   El segundo objeto de exclusión mutua incluye las secuencias 4, 5 y 6, mutuamente excluyentes por velocidad de bits. Cada flujo tiene su propio registro.
-   El tercer objeto de exclusión mutua incluye 7, 8 y 9, mutuamente excluyente según la velocidad de bits. Cada flujo tiene su propio registro.
-   El cuarto objeto de exclusión mutua contiene tres registros, el primero incluye los flujos 1, 2 y 3; el segundo incluye los flujos 4, 5 y 6; y la tercera, incluidas las secuencias 7, 8 y 9. Estos registros se excluyen mutuamente por lenguaje.

Al reproducir un archivo creado de esta manera, la aplicación de transmisión por secuencias selecciona primero el idioma, ya que es menos probable que cambie en medio de la presentación y, a continuación, seleccione una velocidad de bits.

## <a name="mutual-exclusion-object-creation-and-configuration"></a>Creación y configuración de objetos de exclusión mutua

En la lista siguiente se resume el proceso de configuración de un objeto de exclusión mutua:

1.  Cree un objeto de exclusión mutua.
2.  Establezca el tipo de exclusión mutua.
3.  Configure el objeto de exclusión mutua agregando registros y las secuencias asociadas.
4.  Agregue el objeto de exclusión mutua al perfil.

Para crear y configurar un objeto de exclusión mutua

1.  Llame a [**IMFASFProfile:: CreateMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createmutualexclusion) para crear un objeto de exclusión mutua vacío.
2.  Llame a [**IMFASFMutualExclusion:: SetType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-settype) para establecer el criterio de la secuencia mutuamente excluyente.

    Los flujos se pueden excluir mutuamente según el lenguaje, la velocidad de bits, la presentación y los criterios personalizados. El tipo se representa como un GUID. Para obtener una lista de estas constantes, consulte los [GUID de tipo de exclusión mutua de ASF](asf-mutual-exclusion-type-guids.md).

3.  Llame a [**IMFASFMutualExclusion:: AddRecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-addrecord) para agregar un registro al objeto de exclusión mutua.

    Este método agrega un registro vacío y lo asigna a un índice de registro que empieza por cero.

4.  Llame a [**IMFASFMutualExclusion:: AddStreamForRecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-addstreamforrecord) para agregar el número de secuencia al registro especificado por el índice de registro.

    Cada registro incluye una o varias secuencias. Cada secuencia de un registro es mutuamente excluyente de todas las secuencias en cada registro. Para obtener el número de secuencias en un registro, llame a [**IMFASFMutualExclusion:: GetStreamsForRecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-getstreamsforrecord) especificando el índice de registro.

    Para quitar una secuencia del registro, llame a [**IMFASFMutualExclusion:: RemoveStreamFromRecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-removestreamfromrecord) y especifique el índice de registro y el número de secuencia.

5.  Llame a [**IMFASFProfile:: AddMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-addmutualexclusion) para agregar el objeto de exclusión mutua configurado al perfil.

## <a name="enumerating-mutual-exclusion-objects-in-a-profile"></a>Enumerar objetos de exclusión mutua en un perfil

Si [**IMFASFProfile:: AddMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-addmutualexclusion) se realiza correctamente, asigna un índice al objeto especificado, empezando por cero.

Para enumerar los objetos de exclusión mutua asociados a un perfil, llame a [**IMFASFProfile:: GetMutualExclusionCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getmutualexclusioncount) y recorra la lista llamando a [**IMFASFProfile:: GetMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getmutualexclusion). Los índices de exclusión mutua son secuenciales y oscilan entre 0 y uno menos que el número de secuencias recuperadas por **GetMutualExclusionCount**.

Un objeto de exclusión mutua se quita del perfil mediante una llamada a [**IMFASFProfile:: RemoveMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removemutualexclusion). El perfil reasigna los índices de exclusión mutua para que sean secuenciales empezando por cero. Esto sobrescribe los índices previamente almacenados, que ya no son válidos después de llamar a este método. Esto libera los registros de flujo de exclusión mutua asociados.

## <a name="removing-records-in-a-mutual-exclusion-object"></a>Quitar registros de un objeto de exclusión mutua

Para quitar un registro de un objeto de exclusión mutua, llame a [**IMFASFMutualExclusion:: RemoveRecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-removerecord). Si este método se ejecuta correctamente, el objeto de exclusión mutua indexa los registros restantes para que sean secuenciales a partir de cero. La aplicación debe enumerar los registros para garantizar el índice correcto para cada registro. Para ello, llame a [**IMFASFMutualExclusion:: GetRecordCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-getrecordcount) y recorra los registros mediante una llamada a [**IMFASFMutualExclusion:: GetStreamsForRecord**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-getstreamsforrecord).

Quitar el registro con el índice más alto no tiene ningún efecto en los demás índices.

## <a name="modifying-a-mutual-exclusion-object"></a>Modificar un objeto de exclusión mutua

Para cambiar la configuración del objeto de exclusión mutua en el perfil, la aplicación debe reemplazar el objeto de exclusión mutua existente por otro objeto que contenga la nueva configuración.

Para cambiar la configuración del objeto de exclusión mutua en el perfil

1.  Enumere los objetos de exclusión mutua en el perfil para obtener el objeto que se debe cambiar.
2.  Llame a [**IMFASFMutualExclusion:: Clone**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-clone) para clonar el objeto de exclusión mutua.

3.  Configure el objeto clonado según sea necesario.
4.  Llame a [**IMFASFProfile:: RemoveMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removemutualexclusion) para quitar el objeto de exclusión mutua anterior del perfil.

5.  Llame a [**IMFASFProfile:: AddMutualExclusion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-addmutualexclusion) para agregar el objeto de exclusión mutua actualizado al perfil.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Perfil ASF](asf-profile.md)
</dt> </dl>

 

 



