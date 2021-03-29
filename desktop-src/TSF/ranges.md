---
title: Intervalos
description: Intervalos
ms.assetid: 7488e29e-3409-4db3-98b4-f3438ad7c94e
keywords:
- Text Services Framework (TSF), intervalos
- TSF (marco de trabajo de servicios de texto), intervalos
- servicios de texto, intervalos
- Aplicaciones habilitadas para TSF, intervalos
- ranges
- Text Services Framework (TSF), delimitadores
- TSF (marco de trabajo de servicios de texto), delimitadores
- servicios de texto, delimitadores
- Aplicaciones habilitadas para TSF, delimitadores
- delimitadores
- Marco de trabajo de servicios de texto (TSF), clones
- TSF (marco de trabajo de servicios de texto), clones
- servicios de texto, clones
- Aplicaciones habilitadas para TSF, clones
- clones
- Text Services Framework (TSF), copias de seguridad
- TSF (marco de trabajo de servicios de texto), copias de seguridad
- servicios de texto, copias de seguridad
- Aplicaciones habilitadas para TSF, copias de seguridad
- backups
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8c6430f28731f95c0ad9c1beb04b31f0600b8c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994568"
---
# <a name="ranges"></a><span data-ttu-id="4f219-123">Intervalos</span><span class="sxs-lookup"><span data-stu-id="4f219-123">Ranges</span></span>

## <a name="anchors"></a><span data-ttu-id="4f219-124">Delimitadores</span><span class="sxs-lookup"><span data-stu-id="4f219-124">Anchors</span></span>

<span data-ttu-id="4f219-125">Un intervalo está delimitado por dos *delimitadores*, un delimitador inicial y un delimitador final.</span><span class="sxs-lookup"><span data-stu-id="4f219-125">A range is delimited by two *anchors*, a start anchor and an end anchor.</span></span> <span data-ttu-id="4f219-126">Existe un delimitador en una ranura imaginaria entre dos caracteres.</span><span class="sxs-lookup"><span data-stu-id="4f219-126">An anchor exists in an imaginary slot between two characters.</span></span> <span data-ttu-id="4f219-127">El delimitador de inicio se relaciona con el texto que sigue al delimitador y el delimitador final se relaciona con el texto que precede al delimitador.</span><span class="sxs-lookup"><span data-stu-id="4f219-127">The start anchor relates to text that follows the anchor and the end anchor relates to text that precedes the anchor.</span></span> <span data-ttu-id="4f219-128">Los delimitadores inicial y final pueden existir en la misma ubicación.</span><span class="sxs-lookup"><span data-stu-id="4f219-128">Both the start and end anchors can exist in the same location.</span></span> <span data-ttu-id="4f219-129">En este caso, el intervalo tiene una longitud de cero.</span><span class="sxs-lookup"><span data-stu-id="4f219-129">In this case, the range has zero length.</span></span>

<span data-ttu-id="4f219-130">Por ejemplo, empiece con el texto siguiente:</span><span class="sxs-lookup"><span data-stu-id="4f219-130">For example, start with the following text:</span></span>


```C++
This is text.
```



<span data-ttu-id="4f219-131">Ahora aplique un intervalo a este texto con los delimitadores inicial y final en la posición 0.</span><span class="sxs-lookup"><span data-stu-id="4f219-131">Now apply a range to this text with both the start and end anchors at position 0.</span></span> <span data-ttu-id="4f219-132">Se representa visualmente como:</span><span class="sxs-lookup"><span data-stu-id="4f219-132">It is visually represented as:</span></span>


```C++
<anchor></anchor>This is text.
```



<span data-ttu-id="4f219-133">Los delimitadores no ocupan espacio en el propio texto.</span><span class="sxs-lookup"><span data-stu-id="4f219-133">The anchors do not take up any space within the text itself.</span></span> <span data-ttu-id="4f219-134">Este es un intervalo de longitud cero y su texto está vacío.</span><span class="sxs-lookup"><span data-stu-id="4f219-134">This is a zero-length range and its text is empty.</span></span>

<span data-ttu-id="4f219-135">Ahora, desplace el anclaje final + 3 posiciones.</span><span class="sxs-lookup"><span data-stu-id="4f219-135">Now shift the end anchor +3 positions.</span></span> <span data-ttu-id="4f219-136">Se representa visualmente como:</span><span class="sxs-lookup"><span data-stu-id="4f219-136">It is visually represented as:</span></span>


```C++
<anchor>Thi</anchor>s is text.
```



<span data-ttu-id="4f219-137">El delimitador inicial se coloca justo delante del carácter en la posición 0 y el delimitador final se coloca justo después del carácter de la posición 3 porque el delimitador final se desplazó a los 3 lugares correctos.</span><span class="sxs-lookup"><span data-stu-id="4f219-137">The start anchor is positioned just before the character in position 0 and the end anchor is positioned just after the character in position 3 because the end anchor moved to the right 3 places.</span></span> <span data-ttu-id="4f219-138">El intervalo de texto es ahora "Thi".</span><span class="sxs-lookup"><span data-stu-id="4f219-138">The range of text is now "Thi".</span></span>

<span data-ttu-id="4f219-139">Además, no se puede hacer que el delimitador de inicio siga el delimitador final y no se puede establecer el delimitador final para que preceda al delimitador inicial.</span><span class="sxs-lookup"><span data-stu-id="4f219-139">Additionally, the start anchor cannot be made to follow the end anchor and the end anchor cannot be made to precede the start anchor.</span></span>

## <a name="anchor-gravity"></a><span data-ttu-id="4f219-140">Gravedad del anclaje</span><span class="sxs-lookup"><span data-stu-id="4f219-140">Anchor Gravity</span></span>

<span data-ttu-id="4f219-141">Cada delimitador tiene un valor de *gravedad* que determina cómo responde el delimitador cuando se inserta texto en la secuencia de texto en la posición del delimitador.</span><span class="sxs-lookup"><span data-stu-id="4f219-141">Each anchor has a *gravity* setting that determines how the anchor responds when text is inserted into the text stream at the anchor position.</span></span> <span data-ttu-id="4f219-142">Cuando se realiza una inserción en la posición de un delimitador, se debe realizar un ajuste en la posición del delimitador.</span><span class="sxs-lookup"><span data-stu-id="4f219-142">When an insertion is made at the position of an anchor, an adjustment must be made in the position of the anchor.</span></span> <span data-ttu-id="4f219-143">La gravedad determina cómo se realiza este ajuste de posición de delimitador.</span><span class="sxs-lookup"><span data-stu-id="4f219-143">The gravity determines how this anchor position adjustment is made.</span></span>

<span data-ttu-id="4f219-144">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="4f219-144">For example:</span></span>


```C++
It is <anchor></anchor>cold today.
```



<span data-ttu-id="4f219-145">Si la palabra "Very" se inserta en la posición del intervalo, el delimitador inicial puede colocarse antes o después de la palabra insertada:</span><span class="sxs-lookup"><span data-stu-id="4f219-145">If the word "very " is inserted at the range position, the start anchor can be positioned either before or after the inserted word:</span></span>


```C++
It is <anchor>very </anchor>cold today.
```



<span data-ttu-id="4f219-146">\- O bien</span><span class="sxs-lookup"><span data-stu-id="4f219-146">\- Or -</span></span>


```C++
It is very <anchor></anchor>cold today.
```



<span data-ttu-id="4f219-147">La gravedad del anclaje especifica cómo se cambia la posición del delimitador cuando se realiza una inserción en su posición.</span><span class="sxs-lookup"><span data-stu-id="4f219-147">The anchor gravity specifies how the anchor is repositioned when an insertion is made at its position.</span></span> <span data-ttu-id="4f219-148">La gravedad puede ser *hacia atrás* o *hacia delante*.</span><span class="sxs-lookup"><span data-stu-id="4f219-148">The gravity can be either *backward* or *forward*.</span></span>

<span data-ttu-id="4f219-149">Si el delimitador tiene gravedad anterior, el delimitador se desplaza hacia atrás, con respecto al punto de inserción, en la inserción para que el texto insertado siga el delimitador:</span><span class="sxs-lookup"><span data-stu-id="4f219-149">If the anchor has backward gravity, the anchor moves backward, relative to the insertion point, on insertion so that the inserted text follows the anchor:</span></span>


```C++
It is <anchor>very </anchor>cold today.
```



<span data-ttu-id="4f219-150">Si el delimitador tiene gravedad de avance, el delimitador se desplaza hacia delante (en relación con el punto de inserción) en la inserción para que el texto insertado preceda al delimitador:</span><span class="sxs-lookup"><span data-stu-id="4f219-150">If the anchor has forward gravity, the anchor moves forward (relative to the insertion point) on insertion so that the inserted text precedes the anchor:</span></span>


```C++
It is very <anchor></anchor>cold today.
```



## <a name="clones-and-backups"></a><span data-ttu-id="4f219-151">Clones y copias de seguridad</span><span class="sxs-lookup"><span data-stu-id="4f219-151">Clones and Backups</span></span>

<span data-ttu-id="4f219-152">Hay dos formas de hacer una "copia" de un objeto de intervalo.</span><span class="sxs-lookup"><span data-stu-id="4f219-152">There are two ways to make a "copy" of a range object.</span></span> <span data-ttu-id="4f219-153">El primero es crear un *clon* del intervalo mediante [ITfRange:: Clone](/windows/desktop/api/Msctf/nf-msctf-itfrange-clone).</span><span class="sxs-lookup"><span data-stu-id="4f219-153">The first is to make a *clone* of the range using [ITfRange::Clone](/windows/desktop/api/Msctf/nf-msctf-itfrange-clone).</span></span> <span data-ttu-id="4f219-154">La segunda consiste en realizar una *copia de seguridad* del intervalo mediante [ITfContext:: CreateRangeBackup](/windows/desktop/api/Msctf/nf-msctf-itfcontext-createrangebackup).</span><span class="sxs-lookup"><span data-stu-id="4f219-154">The second is to make a *backup* of the range using [ITfContext::CreateRangeBackup](/windows/desktop/api/Msctf/nf-msctf-itfcontext-createrangebackup).</span></span>

<span data-ttu-id="4f219-155">Un clon es una copia de un intervalo que no incluye datos estáticos.</span><span class="sxs-lookup"><span data-stu-id="4f219-155">A clone is a copy of a range that does not include static data.</span></span> <span data-ttu-id="4f219-156">Los delimitadores del intervalo se copian, pero el clon todavía cubre un intervalo de texto dentro del contexto.</span><span class="sxs-lookup"><span data-stu-id="4f219-156">The anchors of the range are copied, but the clone still covers a range of text within the context.</span></span> <span data-ttu-id="4f219-157">Un clon es un objeto de intervalo en todos los aspectos.</span><span class="sxs-lookup"><span data-stu-id="4f219-157">A clone is a range object in all respects.</span></span> <span data-ttu-id="4f219-158">Esto significa que el texto y las propiedades de un intervalo clonado son dinámicos y cambiarán si cambia el texto o las propiedades del intervalo que abarca el clon.</span><span class="sxs-lookup"><span data-stu-id="4f219-158">This means that the text and properties for a cloned range are dynamic and will change if the text and/or properties of the range covered by the clone changes.</span></span>

<span data-ttu-id="4f219-159">Una copia de seguridad almacena el texto y las propiedades de un intervalo en el momento en que se realiza la copia de seguridad como datos estáticos.</span><span class="sxs-lookup"><span data-stu-id="4f219-159">A backup stores the text and properties of a range at the time the backup is made as static data.</span></span> <span data-ttu-id="4f219-160">Una copia de seguridad también clona el intervalo original para que se pueda realizar un seguimiento de los cambios en el tamaño y la posición del intervalo original.</span><span class="sxs-lookup"><span data-stu-id="4f219-160">A backup also clones the original range so that changes to the size and position of the original range can be tracked.</span></span> <span data-ttu-id="4f219-161">Esto significa que el texto y las propiedades de un intervalo del que se ha realizado una copia de seguridad son estáticos y no cambian si cambia el texto o las propiedades del intervalo que abarca la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="4f219-161">This means that the text and properties for a backed up range are static and do not change if the text and/or properties of the range covered by the backup changes.</span></span>

<span data-ttu-id="4f219-162">Por ejemplo, el intervalo siguiente (pRange) en el contexto:</span><span class="sxs-lookup"><span data-stu-id="4f219-162">For example, the following range (pRange) within the context:</span></span>


```C++
"This is some <pRange>text</pRange>."
```



<span data-ttu-id="4f219-163">Ahora cree un clon y una copia de seguridad de este intervalo:</span><span class="sxs-lookup"><span data-stu-id="4f219-163">Now make a clone and a backup of this range:</span></span>


```C++
ITfRange *pClone;
ITfRangeBackup *pBackup;

pRange->Clone(&pClone);
pContext->CreateRangeBackup(ec, pRange, &pBackup);
```



<span data-ttu-id="4f219-164">Ahora, los objetos contienen lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="4f219-164">Now, the objects contain the following:</span></span>


```C++
pRange  = "text"
pClone  = "text"
pBackup = "text"
```



<span data-ttu-id="4f219-165">Ahora cambie el texto de pRange:</span><span class="sxs-lookup"><span data-stu-id="4f219-165">Now change the text of pRange:</span></span>


```C++
WCHAR wsz[] = L"other words";
pRange->SetText(ec, 0, wsz, lstrlenW(wsz));
```



<span data-ttu-id="4f219-166">Ahora, los objetos contienen lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="4f219-166">Now, the objects contain the following:</span></span>


```C++
Context = "This is some other words."
pRange  = "other words"
pClone  = "other words"
pBackup = "text"
```



<span data-ttu-id="4f219-167">Al establecer el texto, el texto del contexto debe cambiar.</span><span class="sxs-lookup"><span data-stu-id="4f219-167">Setting the text caused the text within the context to change.</span></span> <span data-ttu-id="4f219-168">También causó el cambio del delimitador final de pRange y pClone.</span><span class="sxs-lookup"><span data-stu-id="4f219-168">It also caused the end anchor of pRange and pClone to change.</span></span> <span data-ttu-id="4f219-169">pClone Now contiene "otras palabras" porque el texto cambió dentro del intervalo y todos los intervalos realizan el seguimiento de estos cambios.</span><span class="sxs-lookup"><span data-stu-id="4f219-169">pClone now contains "other words" because the text changed within the range and these changes are tracked by all ranges.</span></span> <span data-ttu-id="4f219-170">Cuando cambia el texto incluido en pRange y pClone, el texto de pClone también cambia.</span><span class="sxs-lookup"><span data-stu-id="4f219-170">When the text covered by both pRange and pClone changed, the text of pClone changed as well.</span></span>

<span data-ttu-id="4f219-171">El texto de pBackup no ha cambiado con respecto a la pRange original porque los datos (texto y propiedades) de la copia de seguridad no están relacionados con el contexto y se almacenan por separado.</span><span class="sxs-lookup"><span data-stu-id="4f219-171">The text in pBackup has not changed from the original pRange because the data (text and properties) in the backup is unrelated to the context and is stored separately.</span></span> <span data-ttu-id="4f219-172">El clon contenido en la copia de seguridad cambia realmente, pero los datos son estáticos.</span><span class="sxs-lookup"><span data-stu-id="4f219-172">The clone contained within the backup does actually change, but the data is static.</span></span>

<span data-ttu-id="4f219-173">Al restaurar una copia de seguridad, la copia de seguridad se puede aplicar al clon dentro de la copia de seguridad o a un intervalo diferente completamente.</span><span class="sxs-lookup"><span data-stu-id="4f219-173">When restoring a backup, the backup can be applied to the clone within the backup or to a different range entirely.</span></span> <span data-ttu-id="4f219-174">Para aplicar la copia de seguridad al clon dentro de la copia de seguridad, pase **null** a [ITfRangeBackup:: restore](/windows/desktop/api/Msctf/nf-msctf-itfrangebackup-restore) como se muestra en el ejemplo de código siguiente:</span><span class="sxs-lookup"><span data-stu-id="4f219-174">To apply the backup to the clone within the backup, pass **NULL** to [ITfRangeBackup::Restore](/windows/desktop/api/Msctf/nf-msctf-itfrangebackup-restore) as shown in the following code example:</span></span>


```C++
pBackup->Restore(ec, NULL);
```



<span data-ttu-id="4f219-175">Ahora, los objetos contienen lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="4f219-175">Now, the objects contain the following:</span></span>


```C++
Context = "This is some text."
pRange  = "text"
pClone  = "text"
pBackup = "text"
```



<span data-ttu-id="4f219-176">Para restaurar la copia de seguridad en un intervalo diferente, pase un puntero al objeto de intervalo al llamar a **ITfRangeBackup:: restore**.</span><span class="sxs-lookup"><span data-stu-id="4f219-176">To restore the backup to a different range, pass a pointer to the range object when calling **ITfRangeBackup::Restore**.</span></span> <span data-ttu-id="4f219-177">El texto y las propiedades de las copias de seguridad se aplicarán al nuevo intervalo.</span><span class="sxs-lookup"><span data-stu-id="4f219-177">The backed up text and properties will be applied to the new range.</span></span> <span data-ttu-id="4f219-178">Por ejemplo, si usa el ejemplo anterior antes de la llamada a **restore** , pRange se modificará para demostrar esto:</span><span class="sxs-lookup"><span data-stu-id="4f219-178">For example, using the example above prior to the **Restore** call, pRange will be modified to demonstrate this:</span></span>


```C++
LONG lShifted;
pRange->ShiftEnd(ec, -2, &lShifted, NULL);
```



<span data-ttu-id="4f219-179">Ahora, los objetos contienen lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="4f219-179">Now, the objects contain the following:</span></span>


```C++
Context = "This is some other words."
pRange  = "other wor"
pClone  = "other words"
pBackup = "text"
```



<span data-ttu-id="4f219-180">Cuando el delimitador final de pRange se ha desplazado a la izquierda dos lugares, el delimitador final de pClone no cambió.</span><span class="sxs-lookup"><span data-stu-id="4f219-180">When the end anchor of pRange was shifted to the left two places, the end anchor of pClone did not change.</span></span>

<span data-ttu-id="4f219-181">Ahora restaure la copia de seguridad con pRange con el siguiente ejemplo de código:</span><span class="sxs-lookup"><span data-stu-id="4f219-181">Now restore the backup using pRange with the following code example:</span></span>


```C++
pBackup->Restore(ec, pRange);
```



<span data-ttu-id="4f219-182">Ahora, los objetos contienen lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="4f219-182">Now, the objects contain the following:</span></span>


```C++
Context = "This is some textds."
pRange  = "text"
pClone  = "textds"
pBackup = "text"
```



<span data-ttu-id="4f219-183">El texto que se incluye en pRange se ha reemplazado por "Text", una parte del texto que incluye pClone ha cambiado y pBackup cambia para coincidir con pRange.</span><span class="sxs-lookup"><span data-stu-id="4f219-183">The text covered by pRange has been replaced with "text", a portion of the text covered by pClone has changed, and pBackup changes to match pRange.</span></span>

 

 




