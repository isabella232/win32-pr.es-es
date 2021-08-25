---
description: 'Más información sobre: JET_DBINFOMISC miembros'
title: 'Miembros de JET_DBINFOMISC '
TOCTitle: JET_DBINFOMISC members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_DBINFOMISC
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfomisc_members(v=EXCHG.10)
ms:contentKeyID: 39515834
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 50028b810184b9562a4175e50e72d0ac8cb2ba1e61c76c134ba2c1fbcd4e7533
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119968435"
---
# <a name="jet_dbinfomisc-members"></a>Miembros de JET_DBINFOMISC 

Incluir miembros protegidos  
Incluir miembros heredados  

Contiene información miscelánea sobre una base de datos. Esta es la información contenida en el encabezado de la base de datos.

El [JET_DBINFOMISC](./jet-dbinfomisc-class.md) muestra los miembros siguientes.

## <a name="constructors"></a>Constructores

<table>
<thead>
<tr class="header">
<th> </th>
<th>Nombre</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="hh566519(v=exchg.10).md">JET_DBINFOMISC</a></td>
<td></td>
</tr>
</tbody>
</table>


Superior

## <a name="properties"></a>Propiedades

<table>
<thead>
<tr class="header">
<th> </th>
<th>Nombre</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="hh578821(v=exchg.10).md">bkinfoCopyPrev</a></td>
<td>Obtiene información sobre la última copia de seguridad correcta.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="hh565264(v=exchg.10).md">bkinfoDiffPrev</a></td>
<td>Obtiene información sobre la última copia de seguridad diferencial correcta. Se restablece <a href="hh577635(v=exchg.10).md">cuando se establece bkinfoFullPrev.</a></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="hh577657(v=exchg.10).md">bkinfoFullCur</a></td>
<td>Obtiene información sobre la copia de seguridad actual.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="hh577635(v=exchg.10).md">bkinfoFullPrev</a></td>
<td>Obtiene información sobre la última copia de seguridad completa correcta.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="hh564433(v=exchg.10).md">bkinfoIncPrev</a></td>
<td>Obtiene información sobre la última copia de seguridad incremental correcta. Este valor se restablece cuando <a href="hh577635(v=exchg.10).md">se establece bkinfoFullPrev.</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="hh578850(v=exchg.10).md">cbPageSize</a></td>
<td>Obtiene el tamaño de página de la base de datos. Un valor de 0 significa páginas de 4 Kb.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="hh558061(v=exchg.10).md">dbstate</a></td>
<td>Obtiene el estado coherente o incoherente de la base de datos.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="hh566598(v=exchg.10).md">dwBuildNumber</a></td>
<td>Obtiene el número de compilación del sistema operativo de la última asociación.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="hh578966(v=exchg.10).md">dwMajorVersion</a></td>
<td>Obtiene la versión principal del sistema operativo de la última asociación.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="hh596571(v=exchg.10).md">dwMinorVersion</a></td>
<td>Obtiene la versión secundaria del sistema operativo de la última asociación.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="hh564660(v=exchg.10).md">fShadowingDisabled</a></td>
<td>Obtiene un valor que indica si está habilitado el sombreado de catálogo. Este valor es solo para uso interno.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="hh565757(v=exchg.10).md">fUpgradeDb</a></td>
<td>Obtiene un valor que indica si la base de datos se está actualizando. Este valor es solo para uso interno.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="hh579055(v=exchg.10).md">genCommitted</a></td>
<td>Obtiene la generación máxima de registros confirmados en la base de datos. Normalmente, la generación de registros actual.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="hh579109(v=exchg.10).md">genMaxRequired</a></td>
<td>Obtiene la generación máxima de registros necesaria para reproducir los registros.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="hh565891(v=exchg.10).md">genMinRequired</a></td>
<td>Obtiene la generación mínima de registros necesaria para reproducir los registros. Normalmente, la generación de puntos de control.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="hh577443(v=exchg.10).md">lgposAttach</a></td>
<td>Obtiene los lgpos de la última asociación.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="hh163307(v=exchg.10).md">lgposConsistent</a></td>
<td>Obtiene los lgpos cuando la base de datos se ha hecho coherente. Este valor es NULL si la base de datos es incoherente.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="hh566733(v=exchg.10).md">lgposDetach</a></td>
<td>Obtiene los lgpos de la última desasoción.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="hh564456(v=exchg.10).md">logtimeAttach</a></td>
<td>Obtiene la hora a la que se ha adjuntado la base de datos.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="hh566711(v=exchg.10).md">logtimeBadChecksum</a></td>
<td>Obtiene la última vez que se encontró un error de suma de comprobación no corregible.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="hh557946(v=exchg.10).md">logtimeConsistent</a></td>
<td>Obtiene la hora a la que se hizo coherente la base de datos. Este valor es NULL si la base de datos es incoherente.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="hh556940(v=exchg.10).md">logtimeDetach</a></td>
<td>Obtiene la hora de la última desasoción.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="hh557356(v=exchg.10).md">logtimeECCFixFail</a></td>
<td>Obtiene la última vez que se encontró un error de un bit incorregible.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="hh578967(v=exchg.10).md">logtimeECCFixSuccess</a></td>
<td>Obtiene la última vez que se corrigió correctamente un error de un bit.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="hh577625(v=exchg.10).md">logtimeGenMaxCreate</a></td>
<td>Obtiene la hora de creación del <a href="hh579109(v=exchg.10).md">archivo de registro genMaxRequired.</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="hh579510(v=exchg.10).md">logtimeRepair</a></td>
<td>Obtiene la última vez que se ha ejecutado la reparación en esta base de datos.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="hh565142(v=exchg.10).md">lSPNumber</a></td>
<td>Obtiene el número de Service Pack del sistema operativo de la última asociación.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="hh564996(v=exchg.10).md">signDb</a></td>
<td>Obtiene la firma de la base de datos.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="hh578351(v=exchg.10).md">signLog</a></td>
<td>Obtiene la firma del archivo de registro de los registros usados para modificar la base de datos.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="hh596347(v=exchg.10).md">ulBadChecksum</a></td>
<td>Obtiene el número de veces que se encontró un error de suma de comprobación no corregible.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="hh557876(v=exchg.10).md">ulBadChecksumOld</a></td>
<td>Obtiene el número de veces que se encontró un error de suma de comprobación no corregible antes de la última reparación.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="hh566254(v=exchg.10).md">ulECCFixFail</a></td>
<td>Obtiene el número de veces que se encontró un error de un bit incorregible.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="hh564490(v=exchg.10).md">ulECCFixFailOld</a></td>
<td>Obtiene el número de veces que se encontró un error de un bit incorregible.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="hh578574(v=exchg.10).md">ulECCFixSuccess</a></td>
<td>Obtiene el número de veces que se corrigió correctamente un error de un bit.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="hh578638(v=exchg.10).md">ulECCFixSuccessOld</a></td>
<td>Obtiene el número de veces que se corrigió correctamente un error de un bit antes de la última reparación.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="hh579357(v=exchg.10).md">ulRepairCount</a></td>
<td>Obtiene el número de veces que se ha llamado a la reparación en esta base de datos.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="hh557020(v=exchg.10).md">ulRepairCountOld</a></td>
<td>Obtiene el número de veces que esta base de datos se reparó antes del último desfragmentador.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="hh596219(v=exchg.10).md">ulUpdate</a></td>
<td>Obtiene la versión incremental de Esent que creó la base de datos.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="hh577854(v=exchg.10).md">ulVersion</a></td>
<td>Obtiene la versión de Esent que creó la base de datos.</td>
</tr>
</tbody>
</table>


Superior

## <a name="methods"></a>Métodos

<table>
<thead>
<tr class="header">
<th> </th>
<th>Nombre</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="hh557934(v=exchg.10).md">Equals(Object)</a></td>
<td>Determina si el objeto <a href="/dotnet/api/system.object">especificado</a> es igual al objeto <a href="/dotnet/api/system.object">actual.</a> (Invalida <a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Object.Equals(Object)</a>).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="hh565657(v=exchg.10).md">Equals(JET_DBINFOMISC)</a></td>
<td>Indica si el objeto actual es igual que otro objeto del mismo tipo.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalizar</a></td>
<td>(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="hh558400(v=exchg.10).md">GetHashCode</a></td>
<td>Devuelve el código hash de esta instancia. (Invalida <a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">Object.GetHashCode()</a>).</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gettype#System_Object_GetType">Gettype</a></td>
<td>(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></td>
<td>(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="hh556970(v=exchg.10).md">ToString</a></td>
<td>Obtiene una representación de cadena de este objeto . (Invalida <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>).</td>
</tr>
</tbody>
</table>


Superior

## <a name="see-also"></a>Vea también

#### <a name="reference"></a>Referencia

[JET_DBINFOMISC clase](./jet-dbinfomisc-class.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
